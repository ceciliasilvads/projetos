### Etapa 1: Cálculo de Mortes por 100.000 Habitantes:
A. Utilizamos a função QUERY para filtrar dados específicos de cada país em uma planilha separada.
   
**Exemplo (Peru):**
```
=QUERY(DADOS!A:G, "SELECT A, B, C, E, F, G WHERE A='Peru' AND B>= date '2020-03-02'")
```
**Resultado:** Uma aba nova apenas com dados do páis específico.

![Alt text](image-1.png)


B. Criamos uma nova coluna para calcular as mortes por 100.000 habitantes, usando a população obtida pela função PROCV/VLOOKUP.

Formula Matemática:

    (Número de Mortes * 100.000) / População Total do País

**Formula:**
```
=(F2*100000/VLOOKUP(A2,'População'!A:B,2,false))
```

### Etapa 2: Cálculo do Total Acumulado de Mortes por 100.000 Habitantes:
Adicionamos uma coluna com o número acumulado de óbitos por data, somando os óbitos do periodos anterior com os do periodo mais recente, para as mortes gerais e também por covid-19.



### Etapa 3: Cálculo do Prognóstico de Mortes usando Médias Simples:
Utilizamos a função MÉDIA.SE.S/AVERAGEIFS para calcular a previsão de mortes.

**Exemplo:**
```
=IFERROR(AVERAGEIFS(DADOS!F:F, DADOS!A:A, "=Peru", DADOS!G:G, "=0", DADOS!E:E, D2), I1)
```

### Etapa 4: Cálculo do Excesso de Mortes por COVID:
Subtraímos o número total de mortes notificadas pelo prognóstico de mortes.

**Formula:**

    Total de Mortes por Covid19 no Periodo - Estimativa de Mortes

### Etapa 5: Cálculo do Excesso de Mortes por COVID por 100.000 Habitantes:
Convertemos os números de mortes para valores por 100.000 habitantes, criando uma nova coluna e aplicando a fórmula correspondente.
Formula
$Excesso de Mortes * 100.000 / População do País$

### Etapa 6: Cálculo do Excesso de Mortes por COVID-19 por 100.000 Habitantes Acumuladas:
Similar ao cálculo acumulado de mortes, criaremos uma coluna para o excesso de mortes acumuladas por 100.000 habitantes.