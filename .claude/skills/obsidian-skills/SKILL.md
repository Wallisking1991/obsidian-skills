# obsidian-skills Development Patterns

> Auto-generated skill from repository analysis

## Overview

This codebase manages a collection of skills for Claude Code, organized as individual skill modules with documentation. The project follows a documentation-first approach where each skill is defined by its SKILL.md file and supporting reference materials. The codebase emphasizes clear documentation patterns, standardized skill structures, and plugin marketplace compatibility.

## Coding Conventions

### File Naming
- Use **PascalCase** for TypeScript files: `SkillManager.ts`, `DocumentProcessor.ts`
- Use **lowercase with hyphens** for directories: `obsidian-skills`, `skill-name`
- Use **UPPERCASE** for documentation: `SKILL.md`, `README.md`

### Import/Export Patterns
```typescript
// Mixed import styles - prefer explicit imports
import { SpecificFunction } from './utils';
import * as Utils from './utilities';

// Mixed export styles
export const skillFunction = () => {};
export default SkillManager;
```

### Directory Structure
```
skills/
  skill-name/
    SKILL.md
    references/
      *.md
.claude-plugin/
  plugin.json
  marketplace.json
```

## Workflows

### Single Skill Documentation Update
**Trigger:** When someone wants to improve or fix documentation for one specific skill
**Command:** `/update-skill-docs`

1. Navigate to the specific skill directory: `skills/[skill-name]/`
2. Open the `SKILL.md` file for editing
3. Make targeted improvements to documentation sections
4. Ensure the skill follows the standard SKILL.md format
5. Commit with descriptive message: `docs: update [skill-name] documentation`

### README Enhancement
**Trigger:** When someone wants to improve project documentation or add new setup methods
**Command:** `/update-readme`

1. Identify gaps in current README documentation
2. Open `README.md` in the root directory
3. Add setup instructions, descriptions, or usage examples
4. Ensure consistency with existing documentation style
5. Commit with clear description: `docs: add setup instructions to README`

### Plugin Version Update
**Trigger:** When plugin needs to be updated in the marketplace
**Command:** `/bump-plugin-version`

1. Update version number in `.claude-plugin/plugin.json`
2. Update corresponding metadata in `.claude-plugin/marketplace.json`
3. Ensure version numbers are consistent across both files
4. Update any version-dependent documentation
5. Commit version changes: `docs: bump plugin version to X.Y.Z`

### Multi-Skill Quality Improvement
**Trigger:** When conducting quality review and optimization across multiple skills
**Command:** `/improve-skill-quality`

1. Run evaluation tooling to assess skill quality metrics
2. Identify skills requiring improvements across multiple areas
3. Update multiple `skills/*/SKILL.md` files simultaneously
4. Extract and organize reference materials to `skills/*/references/` directories
5. Commit with detailed metrics: `docs: improve quality across N skills - [specific improvements]`

### Skill Structure Standardization
**Trigger:** When skills need to conform to Agent Skills spec or layout requirements
**Command:** `/standardize-skills`

1. Review current Agent Skills specification requirements
2. Identify skills that don't conform to standard structure
3. Update multiple `skills/*/SKILL.md` files to align with spec
4. Update main `README.md` if structural changes affect usage
5. Ensure consistent formatting across all skill files
6. Commit with alignment description: `docs: align skills with Agent Skills spec`

## Testing Patterns

Tests follow the `*.test.*` naming pattern. While the specific testing framework is not detected, test files should:

```typescript
// Example test structure
describe('SkillManager', () => {
  it('should process skill documentation correctly', () => {
    // Test implementation
  });
});
```

## Commands

| Command | Purpose |
|---------|---------|
| `/update-skill-docs` | Update documentation for a single skill file |
| `/update-readme` | Add setup instructions or descriptions to the main README |
| `/bump-plugin-version` | Update Claude plugin metadata files for marketplace compatibility |
| `/improve-skill-quality` | Comprehensive improvement across multiple skills with reference extraction |
| `/standardize-skills` | Align multiple skills with specification standards |