# Detalhes do projeto

## Dados sobre compartilhamento de bicicletas
Na última década, os sistemas de compartilhamento de bicicletas têm crescido em número e popularidade nas cidades de todo o mundo. Sistemas de compartilhamento de bicicletas permitem que os usuários aluguem bicicletas por um período curtíssimo, por um preço específico. Isso permite que pessoas retirem uma bicicleta do ponto A e a devolvam no ponto B, embora também possam devolvê-la no mesmo local, caso queiram apenas sair para um passeio. Independentemente disso, cada bicicleta pode servir vários usuários por dia.

Graças à ascensão das tecnologias de informação, é fácil para um usuário acessar uma estação dentro do sistema para desbloquear ou devolver as bicicletas. Essas tecnologias também fornecem uma riqueza de dados que podem ser utilizados para explorar como esses sistemas de compartilhamento de bicicletas são usados.

Neste projeto, você usará os dados fornecidos pelo Motivate, um provedor de sistema de bicicletas compartilhadas para diversas grandes cidades dos Estados Unidos, para descobrir os padrões de uso do compartilhamento de bicicletas. Você analisará o uso do sistema de uma das maiores cidades dos Estados Unidos: Chicago.

### Os conjuntos de dados
Os dados para os primeiros seis meses de 2017 são fornecidos. O arquivo de dados contêm seis (6) colunas principais:

- Horário de início (ex., 2017-01-01 00:07:57)
- Horário de término (ex., 2017-01-01 00:20:53)
- Duração da viagem (em segundos, ex., 776)
- Estação inicial (ex., Broadway & Barry Avenue)
- Estação final (ex., Sedgwick St & do North Ave)
- Tipo de usuário (assinante ou cliente)
- Gênero do usuário
- Ano de nascimento do usuário

Os arquivos originais - que podem ser acessados aqui: Chicago, Nova Iorque e Washington - tinham mais colunas, e elas diferiam em formato em muitos casos. Alguns processos de data wrangling foram realizados para condensar esses arquivos nas seis colunas principais citadas acima, para simplificar sua análise e a avaliação de suas habilidades de Python. No curso de data wrangling que sucede este curso no programa, os alunos aprendem a manipular os conjuntos de dados mais obscuros e desorganizados, então não se preocupe em perder algo.

### As perguntas
Você vai escrever um código para completar as seguintes tarefas sobre os dados de compartilhamento de bicicletas:

- Tarefa 1: Mostre as 20 primeiras amostras (linhas) da base de dados
- Tarefa 2: Mostre o gênero (coluna) das 20 primeiras amostras
- Tarefa 3: Cria uma função para pegar colunas como lista
- Tarefa 4: Conte quantas pessoas de cada gênero
- Tarefa 5: Crie uma função para contar os gêneros
- Tarefa 6: Mostre o gênero mais popular
- Tarefa 7: Mostre um gráfico usando os dados anteriores
- Tarefa 8: Responda o motivo do número de homens e mulheres não bater com a quantidade de amostras
- Tarefa 9: Encontre o valor mínimo, máximo, média e mediana da duração de viagens
- Tarefa 10: Mostre todas as estações da base de dados
- Tarefa 11: Confira se documentou todas suas funções
- Tarefa 12: Crie uma função que conte a ocorrência de qualquer coluna (opcional)

## Passo a passo do código

### ToDos
Você deve preencher o código chicago_bikeshare_pt.py nos locais com comentários que começam com "ToDo". Leia todo o código e entenda o fluxo do script e quais partes você deve desenvolver.

### ASSERTs
Nós estamos utilizando assert para garantir que seu código está retornando valores esperados ou que a saída do seu código está no formato correto. NÃO ALTERE ELES. Se você não conseguir passar por um assert, peça ajuda no fórum ou busque ajuda na internet.

O módulo 'csv'
O módulo csv é essencial para a conclusão deste projeto. Um ponto para prestar atenção: esses arquivos CSV de compartilhamento de bicicletas são bastante grandes, então iterá-los vai ser caro computacionalmente. Temos duas estratégias para mitigar isso:

- Não tente abrir o arquivo CSV com um editor de texto. Isso pode travar seu computador.
- Carregue cada arquivo CSV em uma estrutura de dados uma vez no início do script. O código está pronto para ler o arquivo como uma lista de listas (e tudo bem usá-lo assim) Mas você pode trabalhar com outras formas. Dica: Trabalhar com um DictReader, de lista de dicionários, pode ser uma boa opção ([veja esse post no Stack Overflow](https://stackoverflow.com/questions/21572175/convert-csv-file-to-list-of-dictionaries/21572244).)
- Teste regularmente seu código enquanto você o desenvolve. A função print é sua amiga.

Se você estiver familiarizado com o NumPy e/ou Pandas, pode perceber que usar o módulo csv é muito menos eficiente do que essas bibliotecas adaptadas para análise de dados. O módulo csv é utilizado neste projeto para que as habilidades fundamentais de programação possam ser testadas, bem como para obter uma apreciação sobre a velocidade com a qual NumPy e Pandas (que são ensinados mais tarde no programa) podem fazer cálculos em arquivos grandes. Se você já possui habilidades com NumPy e/ou Pandas, não as use. Se não tiver, não se preocupe — essas bibliotecas serão ensinadas em breve.

### Observação
O arquivo **chicago.csv** excede o limite de 100 MB do GitHub. Então, o mesmo será disponibilizado no meu [Google Drive](https://drive.google.com/open?id=1uNYFa-OI8SQcivtvPNjLx3_wGZBpHYAr).