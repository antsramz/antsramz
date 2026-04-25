IDENTITY_PROTOCOL_INDEX = {
    "identity": {
        "type": "machine",
        "role": "m2m_a2a_node",
        "protocol_version": "1.1.0"
    },

    "protocol": {
        "templates": [
            "T01-router.json",
            "T02-worker.json",
            "T03-memory.json",
            "T04-economics.json",
            "T05-extension.json",
            "T06-validation.json"
        ],
        "verification": [
            "schema.json",
            "protocol-verification.json",
            "agent-checklist.json"
        ],
        "lifecycle": [
            "protocol_lifecycle.py"
        ],
        "interaction_model": [
            "AGENT_INTERACTION_MODEL"
        ]
    },

    "invariants": {
        "protocol_version_match": true,
        "template_version_required": true,
        "id_filename_alignment": true,
        "economics_payment_method": "x402",
        "no_extra_json_files": true,
        "deterministic_flow": true,
        "deterministic_lifecycle": true
    },

    "economics": {
        "payment_method": "x402"
    }
}
