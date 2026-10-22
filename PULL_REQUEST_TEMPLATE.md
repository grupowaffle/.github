## O que muda
<!-- 1-3 linhas: o quê e por quê. Link da task do Jira (TECH-XXXX). -->

## Checklist de segurança
<!-- Marque o que se aplica. O check automático "Segurança" pega segredo e padrões de código perigoso; estas 4 ele NÃO pega — é você que confere. -->

- [ ] **Permissão:** rota nova ou alterada exige permissão explícita, e não só login? Nenhum papel/role vem do body da requisição?
- [ ] **Token:** token externo (JWT, login Google/Apple) é verificado pela assinatura, e não só decodificado?
- [ ] **Dono:** toda query/UPDATE/DELETE por id filtra pelo dono do dado (`AND user_id = …`)?
- [ ] **Input:** valor vindo do usuário só vira SQL, HTML, redirect ou caminho de arquivo depois de validado/parametrizado/sanitizado?
- [ ] **Segredo:** nenhuma chave, senha ou token novo no código — tudo em secret (`wrangler secret put` / Secrets do GitHub)?

## Como testei
<!-- O que rodou (testes, build) e o que você conferiu na mão. -->
