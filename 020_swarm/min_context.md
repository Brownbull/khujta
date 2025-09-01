Got it 👍 — let’s design a **standard JSON envelope** that carries the **minimum required context** for any agent call in the NeuroMemory framework, plus optional enrichment fields. This way, every agent can parse a predictable base, while richer agents can use additional detail if provided.

Here’s a clean draft:

```json
{
  "agent_context": {
    "id": "uuid",                // Unique ID for this agent call
    "timestamp": "2025-09-01T12:34:56Z", 

    "caller_identity": {
      "neuro_sig": "sha256-hash", // Required: cryptographic identity of the caller
      "role": "self|peer|co-op|system" // Required: context role for this call
    },

    "memory_reference": {
      "block_id": "uuid",        // Required: the target NeuroBlock or Composite ID
      "access_level": "read|write|transform|share" // Required: what the agent is allowed to do
    },

    "execution": {
      "intent": "retrieve|store|validate|adapt|share", // Required action
      "priority": "normal|urgent"                      // Required for scheduling
    },

    "permissions": {
      "expiry": "2025-12-31T23:59:59Z", // Required: validity of this call
      "delegated_by": "uuid|null"       // Who granted this permission
    }
  },

  "optional_context": {
    "sensory_hints": {
      "modality": ["visual", "auditory"], 
      "intensity_level": "low|medium|high"
    },
    "emotional_tags": ["calm", "nostalgia"], 
    "cultural_frame": "en-US|es-CL|jp-JP", 
    "compression": "raw|lossy|abstracted", 
    "delivery_preferences": {
      "format": "neuro-stream|symbolic|semantic-summary",
      "bandwidth_limit": "512kbps"
    },
    "trust_context": {
      "reputation_score": 0.87, 
      "previous_interactions": 42
    }
  }
}
```

---

### 🔑 Key ideas:

* **`agent_context`** = minimum required context → ensures all calls have identity, intent, and permissioning.
* **`optional_context`** = enrichment layer → allows richer calls (sensory adaptation, cultural fit, compression preferences).
* Agents that don’t understand `optional_context` can safely ignore it.

---

👉 Do you want me to also create a **JSON Schema** (validation spec) for this envelope, so any agent implementation can enforce the required vs optional fields?
