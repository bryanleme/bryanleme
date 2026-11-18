<div align="center">

<img src="assets/scene.svg" alt="Agents de IA caminhando pela cidade: Proc, Sqli, Bia e Auto" width="100%"/>

### Oi, eu sou o Bryan. 👋
**Entendo o processo, converso com o dado e deixo as máquinas fazerem o trabalho chato.**

</div>

<br/>

## 🧭 Em uma frase

Gosto de chegar num processo bagunçado, entender por que ele é do jeito que é e deixá-lo mais simples.
Depois eu construo o que faltava: o indicador que mostra onde agir, a consulta SQL que busca o dado direto na fonte e a automação que tira o trabalho manual da frente de todo mundo.

Venho da indústria, moro no interior de São Paulo e hoje vivo entre **processo, dado e automação**.
Quando alguém pergunta "isso dá pra automatizar?", eu respondo com outra pergunta: *o processo está certo antes?* 😄

<br/>

## 🤖 Meu time (de agents de IA, fictícios, claro)

Toda cidade precisa de uma equipe. A minha anda por aí lá em cima, e cada um tem o seu jeito de trabalhar:

<img src="assets/squad.svg" alt="O time de agents: Proc, Sqli, Bia e Auto" width="100%"/>

> **Proc** pergunta "por quê?" até o problema aparecer. **Sqli** vai buscar o dado na fonte. **Bia** transforma número em decisão. **Auto** assume o trabalho repetitivo e roda de madrugada. Eu só faço o café e confiro se está tudo certo. ☕

<br/>

## 🏆 Quando eles trabalham juntos

<img src="assets/numeros.svg" alt="R$ 7 milhões em ganhos, coleta de 40 para 2 minutos, mais de 400 medidas em DAX, 50 municípios e mais de 60 usuários" width="100%"/>

E tem mais: evitei uma contratação externa (economia estimada de **R$ 200 mil**) ao construir por conta própria a solução de indicadores em Power BI, e fui usuário-chave numa certificação de qualidade automotiva que abriu as portas de uma montadora como cliente.

<br/>

## 💻 Código, simulado

Exemplos fictícios, só para mostrar como a gente pensa por aqui.

<img src="assets/terminal-agents.svg" alt="Terminal simulado com o status do Bryan" width="100%"/>

<details>
<summary>🔎 <b>Sqli:</b> primeiro a gente ataca o que mais dói</summary>

```sql
SELECT   processo,
         COUNT(*)                                          AS ocorrencias,
         ROUND(AVG(tempo_manual_min), 1)                   AS minutos_perdidos,
         ROUND(100 * RATIO_TO_REPORT(COUNT(*)) OVER (), 1) AS pct_do_total
FROM     operacao_simulada
WHERE    status = 'RETRABALHO'
GROUP BY processo
ORDER BY ocorrencias DESC
FETCH FIRST 5 ROWS ONLY;
```

</details>

<details>
<summary>📊 <b>Bia:</b> mostrar o desvio, não só o número</summary>

```dax
Desvio vs Meta % =
VAR Realizado = [Total Realizado]
VAR Meta      = [Total Meta]
RETURN
    IF ( Meta = 0, BLANK (), DIVIDE ( Realizado - Meta, Meta ) )
```

</details>

<details>
<summary>⚙️ <b>Auto:</b> validar, fazer backup, registrar</summary>

```powershell
function Invoke-AutomacaoSegura {
    param([string]$Origem, [string]$Destino)

    Copy-Item $Destino "$Destino.bak" -Force                        # 1. backup antes de mexer
    $dados = Import-Csv $Origem

    if ($dados.Count -eq 0) { throw "Origem vazia, abortando." }    # 2. validação

    $dados | Export-Csv $Destino -NoTypeInformation
    Add-Content "execucoes.log" "$(Get-Date -f s) OK $($dados.Count) linhas"   # 3. registro
}
```

</details>

<br/>

## 🧰 Caixa de ferramentas

| | |
|---|---|
| 🔎 **Dados** | SQL (Oracle), Power BI, DAX, Power Query, Excel avançado |
| ⚙️ **Automação** | Power Automate, Power Apps, SharePoint, PowerShell |
| 🧭 **Processo** | Lean Six Sigma Master Black Belt, DMAIC, PDCA, Kaizen, KPIs |
| 🏭 **Sistemas** | SAP, ERP Protheus |
| 🤖 **IA** | Para prototipar mais rápido, sempre com validação por cima |

<br/>

## 🚀 Projetos públicos

- **[SteelFlow AI](https://github.com/bryanleme/steelFlow-ai)**: ambiente para comparar cenários "e se?" de processo industrial, com faixas P10/P50/P90. Mostra inclusive o resultado que *não* bateu a meta, porque transparência também é parte da análise.
- **[Achei!! Vagas](https://github.com/bryanleme/achei-vagas)**: monitor automatizado de vagas que roda no GitHub Actions e avisa no Telegram.

<br/>

## 📊 GitHub em números

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=bryanleme&show_icons=true&hide_border=true&include_all_commits=true&count_private=true&bg_color=0c1230&title_color=ff8a3d&text_color=ffffff&icon_color=3ddc97" alt="Estatísticas do GitHub"/>

</div>

<br/>

## 📬 Bora conversar?

Estou aberto a conversas sobre vagas que unam **processos, operações e dados**.

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-bryan--leme-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/bryan-leme)

<sub>Personagens originais, criados só para este perfil. 🤖✨</sub>

</div>
