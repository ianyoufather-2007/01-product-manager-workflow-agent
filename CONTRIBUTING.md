# Contributing

Thanks for helping improve this skill.

## Good Contributions

- Clearer decision rules for Amazon product selection, launch, growth, profit, inventory, or stop-loss.
- Better templates for market screening, product selection memos, launch plans, and business reviews.
- Public, non-sensitive examples that show how the skill should behave.
- Fixes that make the skill more portable across marketplaces, categories, or seller sizes.

## Ground Rules

- Do not include private seller data, customer data, supplier quotes, credentials, paid-tool exports, or browser sessions.
- Keep `SKILL.md` concise. Put detailed frameworks or templates in `references/`.
- Prefer reusable instructions over one-off case notes.
- Make assumptions explicit when adding thresholds or scoring logic.

## Local Validation

If you have Codex skill validation scripts available, run validation against:

```text
skills/amazon-product-manager
```

At minimum, check that `SKILL.md` has only `name` and `description` in YAML frontmatter and that referenced files exist.
