# Commit Message Instructions

Écris les messages de commit avec ce format, de façon stricte.

## Format

`type(scope): short summary`

Puis, si utile, un body en puces courtes:

- what changed
- why
- impact/risk

## Rules

- Utiliser un style **Conventional Commits**.
- `type` autorisés: `feat`, `fix`, `refactor`, `perf`, `test`, `docs`, `chore`, `build`, `ci`.
- `scope` doit être précis (ex: `api`, `client`, `draws`, `homepage`, `infra`).
- `short summary`:
  - en anglais
  - au présent
  - concis (max ~72 caractères)
  - orienté résultat
- Body:
  - optionnel
  - puces courtes
  - pas de blabla
  - décrire uniquement ce qui est réellement modifié
- Ne jamais inventer de changement non présent dans le diff.

## Examples

`feat(api): move areuptodate logic from gateway to service`

- remove `AreDrawsUpToDateAsync` from repository contract
- implement up-to-date business logic in `DrawUseCases`
- keep endpoint behavior unchanged

`fix(client): handle null areUpToDate response on homepage`

- guard query result before property access
- prevent runtime crash during loading state

`refactor(infra): simplify draw repository read methods`

- remove redundant mapping steps
- keep query behavior and output unchanged
