# Missions

Missions are the only way work is supposed to happen in this repository.

## Rules

1. Only one mission should be actively worked on at a time unless the human explicitly says otherwise.
2. A mission is not complete until its success criteria are met **and** a field note exists.
3. Agents must not start a blocked mission.
4. After a mission is finished, the human reviews the result before the next mission is unlocked.

## Current mission order

| ID  | Name              | Status          | Depends on     |
|-----|-------------------|-----------------|----------------|
| 00  | Bootstrap         | Ready           | —              |
| 01  | First Model       | Blocked         | 00             |
| 02  | Character Base    | Blocked         | 01             |
| 03  | Tiny Test Zone    | Blocked         | 01 + 02        |

Future missions will be added as earlier ones prove the pipeline.
