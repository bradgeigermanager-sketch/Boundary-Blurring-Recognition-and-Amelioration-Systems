# Provenance Router – JSON Schema

This document defines the JSON schema used by the Provenance Router to ensure every signal carries explicit, auditable origin metadata. The schema enforces clarity of source, intent, routing, and traversal path.

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "$id": "https://example.org/schemas/provenance-router.json",
  "title": "ProvenanceRouterEvent",
  "type": "object",
  "required": [
    "eventId",
    "timestamp",
    "source",
    "signal",
    "routing",
    "provenance"
  ],
  "properties": {
    "eventId": { "type": "string" },
    "timestamp": { "type": "string", "format": "date-time" },

    "source": {
      "type": "object",
      "required": ["domain", "actorType", "actorId"],
      "properties": {
        "domain": {
          "type": "string",
          "enum": ["organizational", "device", "infrastructure", "external"]
        },
        "actorType": { "type": "string" },
        "actorId": { "type": "string" },
        "layer": {
          "type": "string",
          "enum": ["policy", "strategy", "operations", "execution"]
        }
      }
    },

    "signal": {
      "type": "object",
      "required": ["category", "severity", "intent"],
      "properties": {
        "category": { "type": "string" },
        "severity": {
          "type": "string",
          "enum": ["info", "low", "medium", "high", "critical"]
        },
        "intent": {
          "type": "string",
          "enum": ["actionable", "informational", "diagnostic", "test"]
        },
        "payload": { "type": "object" }
      }
    },

    "routing": {
      "type": "object",
      "required": ["targetDomain", "targetActorId", "authorityToAct"],
      "properties": {
        "targetDomain": {
          "type": "string",
          "enum": ["organizational", "device", "infrastructure", "external"]
        },
        "targetActorId": { "type": "string" },
        "authorityToAct": { "type": "boolean" },
        "constraints": {
          "type": "array",
          "items": { "type": "string" }
        }
      }
    },

    "provenance": {
      "type": "object",
      "required": ["path", "originalSource"],
      "properties": {
        "originalSource": {
          "type": "object",
          "required": ["domain", "actorId"],
          "properties": {
            "domain": { "type": "string" },
            "actorId": { "type": "string" }
          }
        },
        "path": {
          "type": "array",
          "items": {
            "type": "object",
            "required": ["via", "timestamp"],
            "properties": {
              "via": { "type": "string" },
              "timestamp": { "type": "string", "format": "date-time" }
            }
          }
        },
        "correlationId": { "type": "string" }
      }
    }
  }
}
