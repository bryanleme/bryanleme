<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:1f6feb,100:58a6ff&height=210&section=header&text=Bryan%20Leme&fontSize=62&fontColor=ffffff&animation=fadeIn&fontAlignY=36&desc=Processos%20%C2%B7%20Dados%20%C2%B7%20Automa%C3%A7%C3%A3o&descSize=20&descAlignY=58" alt="Bryan Leme" width="100%"/>

<a href="https://github.com/bryanleme">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=900&color=58A6FF&center=true&vCenter=true&width=720&lines=Oi%2C+eu+sou+o+Bryan+%F0%9F%91%8B;Especialista+em+processos+e+opera%C3%A7%C3%B5es;que+tamb%C3%A9m+fala+a+l%C3%ADngua+dos+dados;SQL+%C2%B7+Power+BI+%C2%B7+KPIs+%C2%B7+automa%C3%A7%C3%A3o;Primeiro+eu+entendo+o+processo.+Depois+eu+automatizo." alt="Digitando..." />
</a>

<br/><br/>

![Lean Six Sigma](https://img.shields.io/badge/Lean_Six_Sigma-Master_Black_Belt-2ea043?style=for-the-badge)
![SQL](https://img.shields.io/badge/SQL-Oracle-f0883e?style=for-the-badge&logo=oracle&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-DAX-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Power Platform](https://img.shields.io/badge/Power_Apps_%2B_Automate-742774?style=for-the-badge&logo=powerapps&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white)

<img src="https://komarev.com/ghpvc/?username=bryanleme&label=Visitas&color=1f6feb&style=for-the-badge" alt="Visitas"/>

</div>

<br/>

<h2><img src="https://fonts.gstatic.com/s/e/notoemoji/latest/1f44b/512.gif" width="32" height="32" alt="👋"/> Quem sou eu</h2>

Gosto de chegar num processo bagunçado, entender por que ele é do jeito que é e deixá-lo mais simples.
Depois eu construo o que faltava: o indicador que mostra onde agir, a consulta SQL que busca o dado direto na fonte e a automação que tira o trabalho manual da frente de todo mundo.

Venho da indústria, moro no interior de São Paulo e hoje vivo entre **processo, dado e automação**.
Quando alguém pergunta "isso dá pra automatizar?", respondo com outra pergunta: *o processo está certo antes?*

<div align="center">
<img src="assets/caos-ao-controle.svg" alt="Do caos ao controle" width="100%"/>
</div>

<br/>

<h2><img src="https://fonts.gstatic.com/s/e/notoemoji/latest/1f4bb/512.gif" width="32" height="32" alt="💻"/> Meu jeito de pensar, em código (simulado)</h2>

```sql
-- Como eu enxergo um problema operacional (consulta fictícia, só para ilustrar)
SELECT   processo,
         COUNT(*)                                          AS ocorrencias,
         ROUND(AVG(tempo_manual_min), 1)                   AS minutos_perdidos,
         ROUND(100 * RATIO_TO_REPORT(COUNT(*)) OVER (), 1) AS pct_do_total
FROM     operacao_simulada
WHERE    status = 'RETRABALHO'
GROUP BY processo
ORDER BY ocorrencias DESC
FETCH FIRST 5 ROWS ONLY;   -- primeiro eu ataco o que mais dói
```

```dax
// Uma medida que eu gosto: mostra o desvio, não só o número (exemplo fictício)
Desvio vs Meta % =
VAR Realizado = [Total Realizado]
VAR Meta      = [Total Meta]
RETURN
    IF ( Meta = 0, BLANK (), DIVIDE ( Realizado - Meta, Meta ) )
```

```powershell
# Toda automação minha segue a mesma regra: validar, fazer backup, registrar (exemplo fictício)
function Invoke-AutomacaoSegura {
    param([string]$Origem, [string]$Destino)

    Copy-Item $Destino "$Destino.bak" -Force                        # 1. backup antes de mexer
    $dados = Import-Csv $Origem

    if ($dados.Count -eq 0) { throw "Origem vazia, abortando." }    # 2. validação

    $dados | Export-Csv $Destino -NoTypeInformation
    Add-Content "execucoes.log" "$(Get-Date -f s) OK $($dados.Count) linhas"   # 3. registro
}
```

<h2><img src="https://fonts.gstatic.com/s/e/notoemoji/latest/1f3c6/512.gif" width="32" height="32" alt="🏆"/> Alguns números que me deixam orgulhoso</h2>

| O que | Resultado |
|---|---|
| Projeto de revisão de rotas | **R$ 7 milhões** em ganhos validados |
| Solução de indicadores em Power BI feita por conta própria | **Contratação externa evitada** (economia estimada de R$ 200 mil) |
| Etapa de coleta de dados | De **~40 min manuais** para **~2 min** automáticos |
| Painel executivo em Power BI | **400+ medidas em DAX**, ligado direto ao banco corporativo |
| Automações e aplicativo em Power Apps | **7 automações**, **50 municípios**, **60+ usuários** |

<h2><img src="https://fonts.gstatic.com/s/e/notoemoji/latest/1f525/512.gif" width="32" height="32" alt="🔥"/> Minha caixa de ferramentas</h2>

| | |
|---|---|
| **Dados** | SQL (Oracle), Power BI, DAX, Power Query, Excel avançado |
| **Automação** | Power Automate, Power Apps, SharePoint, PowerShell |
| **Processo** | Lean Six Sigma Master Black Belt, DMAIC, PDCA, Kaizen, KPIs |
| **Sistemas** | SAP, ERP Protheus |
| **IA** | Para prototipar mais rápido, sempre com validação por cima |

<h2><img src="https://fonts.gstatic.com/s/e/notoemoji/latest/1f680/512.gif" width="32" height="32" alt="🚀"/> Projetos públicos</h2>

- **[SteelFlow AI](https://github.com/bryanleme/steelFlow-ai)**: ambiente para comparar cenários "e se?" de processo industrial, com faixas P10/P50/P90. Mostra inclusive o resultado que *não* bateu a meta, porque transparência também é parte da análise.
- **[Achei!! Vagas](https://github.com/bryanleme/achei-vagas)**: monitor automatizado de vagas que roda no GitHub Actions e avisa no Telegram.

<h2><img src="https://fonts.gstatic.com/s/e/notoemoji/latest/1f4ca/512.gif" width="32" height="32" alt="📊"/> GitHub em números</h2>

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=bryanleme&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true" alt="Estatísticas do GitHub"/>
<img height="165" src="https://github-readme-streak-stats.herokuapp.com/?user=bryanleme&theme=tokyonight&hide_border=true" alt="Sequência de contribuições"/>

<br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=bryanleme&theme=tokyo-night&hide_border=true&area=true" alt="Gráfico de atividade" width="100%"/>

</div>

<h2><img src="https://fonts.gstatic.com/s/e/notoemoji/latest/1f4ac/512.gif" width="32" height="32" alt="💬"/> Vamos conversar?</h2>

Estou aberto a conversas sobre vagas que unam **processos, operações e dados**.

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-bryan--leme-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/bryan-leme)

<br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:58a6ff,50:1f6feb,100:0d1117&height=120&section=footer" alt="" width="100%"/>

</div>
