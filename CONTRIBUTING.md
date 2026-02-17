# Contribuindo

Se você está com erro para criar Pull Request, siga este fluxo rápido.

## 1) Configure o repositório remoto
Verifique se existe `origin`:

```bash
git remote -v
```

Se não existir, adicione:

```bash
git remote add origin https://github.com/<seu-usuario>/<seu-repo>.git
```

## 2) Crie uma branch de trabalho
```bash
git checkout -b feat/minha-mudanca
```

## 3) Commit das mudanças
```bash
git add .
git commit -m "Minha mudança"
```

## 4) Envie a branch
```bash
git push -u origin feat/minha-mudanca
```

## 5) Abra a Pull Request
### Opção A — Pelo GitHub (web)
Depois do push, abra o repositório no GitHub e clique em **Compare & pull request**.

### Opção B — Pelo GitHub CLI
Se tiver `gh` instalado e autenticado:

```bash
gh pr create --fill
```

## Problemas comuns
- **"No commits between base and head"**: a branch não tem commits novos em relação à base.
- **"Repository not found"**: URL de `origin` errada ou falta permissão.
- **"Permission denied"**: autenticação inválida (token/chave SSH) ou sem acesso ao repo.
- **Não aparece botão de PR**: confira se o push foi para uma branch diferente de `main`.
