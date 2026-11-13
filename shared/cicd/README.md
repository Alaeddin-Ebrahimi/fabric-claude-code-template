# cicd

How changes move from development to production.

- **Git integration:** connect each workspace to a branch, with the Git folder set to that workspace's `items/` folder.
- **Deployment pipelines:** stages such as Dev, Test and Prod, and their rules.
- **Variable library:** values that differ per environment, so items don't hard-code them.
- **Parameter files** go in `parameters/`; helper and deployment scripts in `scripts/`.

Note your branching approach (for example a feature branch per change, merged by pull request) and who approves production releases.
