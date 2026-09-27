# Contributing

Issues and pull requests are welcome, especially real stars that the refusal rules got wrong in
either direction (refused a drivable star, or accepted one no run could satisfy).

## Before you open a PR

1. Run the smoke test. It needs no key and no network:
   ```bash
   python3 scripts/smoke_test.py
   ```
2. If you change what the tool prints or refuses, update the README example that shows it. Every
   claim in the README is asserted by the smoke test, so keep them in step.
3. Stay stdlib-only. No dependencies.

## Ground rules the code keeps

- A judge that cannot answer never passes. A broken answer must never read as agreement.
- An empty evidence file is refused before any judge is asked.
- The gate prints the numbers behind its verdict.
