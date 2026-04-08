# Playbooks — domestic-flights

> CLI command sequences. Knowledge is for parameter mapping — never answer without executing.

---

## Playbook A: Trunk Routes

**Trigger:** "Beijing to Shanghai", "北京到上海"

```bash
flyai search-flight --origin "Beijing" --destination "Shanghai" --dep-date {date} --sort-type 3
```

**Output emphasis:** 30+ daily flights. Show top 5 cheapest.

---

## Playbook B: Budget Airlines

**Trigger:** "cheapest domestic"

```bash
flyai search-flight --origin "{o}" --destination "{d}" --dep-date {date} --sort-type 3
```

**Output emphasis:** Highlight budget airlines (Spring, 9 Air, Lucky Air) with luggage notes.

---

## Playbook C: Regional Airports

**Trigger:** "fly to [small city]"

```bash
flyai search-flight --origin "{o}" --destination "{d}" --dep-date {date} --sort-type 3
# If no results, suggest nearest major airport
```

**Output emphasis:** Try direct, suggest hub connections if needed.

---

