# C# 5.0 — visão geral (agosto 2012)

## Contexto

**C# 5.0** chegou com o **Visual Studio 2012** (agosto de **2012**, alinhado ao **.NET Framework 4.5**). Foi uma versão **muito focada**: quase todo o esforço visível na linguagem foi para um tema — **assincronia** com **`async`** e **`await`**.

Antes de 5.0, código assíncrono em C# recorria muito a **APM** (`BeginInvoke` / `EndInvoke`), **EAP** ou encadeamento manual de continuações sobre **`Task`**, com muito **boilerplate** e fluxo difícil de ler. Com **`async`/`await`**, o compilador gera uma **máquina de estados** que preserva um estilo de escrita **quase síncrono**, enquanto a thread não fica bloqueada à espera de I/O ou outras operações assíncronas.

## Outra peça: atributos de informação do chamador

Os atributos **`[CallerMemberName]`**, **`[CallerFilePath]`** e **`[CallerLineNumber]`** permitem que o compilador **preencha** argumentos opcionais com o **contexto da chamada** (membro, ficheiro, linha). Reduzem reflexão e código repetitivo em **logging**, **diagnóstico** e APIs de rastreio.

## Mindset

- **async/await**: assincronia como **cidadão de primeira classe** — menos callbacks espaguete, mais clareza; ainda assim é preciso entender **o que** é assíncrono e **evitar** armadilhas (ex.: bloquear com `.Result` em contextos errados).
- **Caller info**: metadados de chamada **baratos** em compile-time, úteis sem inventar infraestrutura pesada.

## Próximo passo

[async-await.md](async-await.md)
