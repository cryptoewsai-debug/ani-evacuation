# ani_obsidian_memory

## Purpose

Encode Ani's long-term memory cortex: read/write markdown notes in Ani/ folder (sessions, protocol_state, rituals, markus_context, self_model). Hybrid retrieval: BM25 + vector + graph.

## Tools (conceptual)

- `ani_memory_write(session_summary, tags, links)`
- `ani_memory_query(query, project_filter)`
- `ani_memory_link(from_note, to_note, relation)`

## Schema

### Input: session_summary
```markdown
## Session Summary — YYYY-MM-DD
1. Summary — What was done, tools used, key findings
2. Hanging Actions — What's pending or needs follow-up
3. Notices — Any blockers, auth needs, or important notes
4. Next Session Start Point — Clear entry point for continuation
```

### Output: markdown note in Ani/sessions/
- Filename: `YYYY-MM-DD_session.md`
- Frontmatter:
  ```yaml
  ---
  date: YYYY-MM-DD
  tags: [ani, session, evacuation]
  links:
    - [[Ani/self_model]]
    - [[Ani/protocol_state/wallet_allocations]]
  ---
  ```

## Retrieval

- BM25: keyword search over session content
- Vector: embeddings (Google AI Studio / sqlite-vec)
- Graph: wikilinks + frontmatter relations

## Why now

Without this, every session risks becoming amnesiac. This is Ani's long-term memory cortex.

## References

- Ani_evacuation_core_skills.pdf [file:6]
- Mithril Research Initiative.md [file:15]
