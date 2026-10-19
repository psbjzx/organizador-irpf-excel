# Organizador de Informações para IRPF — Excel

## Sobre o projeto

Este projeto consiste em uma ferramenta desenvolvida no Microsoft Excel para organizar e centralizar informações que podem auxiliar na preparação da declaração do Imposto de Renda Pessoa Física (IRPF).

Desenvolvida a partir de um desafio da DIO, a planilha busca facilitar o preenchimento de dados cadastrais, o registro de receitas e a organização de informações bancárias em uma interface visual estruturada.

O projeto aplica recursos do Excel para melhorar a organização dos dados, orientar o preenchimento de determinados campos e consolidar automaticamente valores informados pelo usuário.

## Objetivos

- Centralizar informações cadastrais do titular.
- Organizar registros de receitas por data, categoria e valor.
- Reunir valores informados em até três instituições financeiras.
- Calcular automaticamente o total dos valores bancários cadastrados.
- Utilizar validação de dados para padronizar determinadas entradas.
- Estruturar a planilha em abas, facilitando a localização das informações.

## Estrutura da planilha

### 1. TITULAR

Aba destinada ao preenchimento das informações cadastrais, incluindo:

- Nome e CPF.
- Data de nascimento e título de eleitor.
- Informações sobre cônjuge.
- Endereço, CEP e contatos.
- Indicadores cadastrais relacionados à declaração anterior, dependente cônjuge e residência no exterior.

Os campos de determinadas informações cadastrais contam com listas de seleção para padronizar as respostas.

### 2. NOTAS

Área destinada ao registro de receitas, organizada em três campos principais:

- **Data:** data do recebimento.
- **Categoria:** classificação do registro.
- **Valor (R$):** valor da receita informada.

A categoria possui opções como Contracheque, CNPJ e Freelance, além de uma opção inicial para seleção.

A estrutura oferece espaço para múltiplos registros, permitindo reunir informações em um único local.

### 3. INFORMES

Aba destinada à organização de informações de até três instituições financeiras.

Para cada instituição, a planilha contém campos para:

- Identificação do banco.
- Valor atual informado.
- Referência visual para um documento em PDF.

O campo de totalização consolida os três valores cadastrados, facilitando a visualização conjunta dos montantes informados.

### 4. Bancos

Aba auxiliar oculta que contém uma relação de instituições financeiras, utilizada como base de apoio para a organização das opções bancárias.

Na versão atual, essa lista ainda precisa ser vinculada aos campos correspondentes da aba INFORMES por meio de validação de dados para permitir a seleção efetiva dos bancos em menus suspensos.

## Recursos técnicos utilizados

- Microsoft Excel.
- Validação de dados por listas.
- Validação de data.
- Fórmulas de soma.
- Referências entre células.
- Organização visual por abas e campos de preenchimento.
- Aba auxiliar para centralização de opções.
- Formatação de valores monetários.

## Funcionamento dos cálculos

Na aba INFORMES, o campo TOTAL utiliza uma fórmula para somar os valores registrados para as três instituições financeiras.

A lógica do cálculo é:

```excel
=SOMA(D14;D19;D24)
```

As referências correspondem aos campos de valor atual de cada instituição financeira.

Dessa forma, ao alterar os valores cadastrados, o total pode ser atualizado automaticamente pelo Excel.

## Como utilizar

1. Abra o arquivo `Renda.xlsx` no Microsoft Excel.
2. Acesse a aba TITULAR e preencha as informações cadastrais.
3. Utilize a aba NOTAS para registrar as receitas, suas datas, categorias e valores.
4. Na aba INFORMES, preencha as instituições financeiras e os respectivos valores atuais.
5. Confira o total consolidado e revise os dados informados.
6. Salve o arquivo preenchido em um local seguro.

## Melhorias futuras

O projeto pode ser aprimorado com a implementação dos seguintes recursos:

- Aplicar a validação de data a todas as linhas disponíveis para registro de receitas.
- Vincular a lista auxiliar de bancos aos campos da aba INFORMES por meio de menus suspensos.
- Implementar links funcionais para acesso aos documentos comprobatórios.
- Adicionar atalhos de navegação entre as abas.
- Ampliar as categorias de receitas e os campos de organização.
- Implementar verificações adicionais para reduzir erros de preenchimento.

## Limitações e considerações

Esta ferramenta tem finalidade organizacional e educacional. Ela não substitui o programa oficial da Receita Federal, não transmite declarações e não calcula automaticamente o imposto devido.

Os campos de anexos representam marcadores visuais e ainda não estão vinculados a documentos PDF na versão atual.

Os dados informados devem ser conferidos pelo usuário, e as regras tributárias aplicáveis precisam ser verificadas nas fontes oficiais.

Antes de compartilhar o arquivo publicamente, substitua eventuais informações pessoais ou financeiras reais por dados fictícios.

## Aprendizados

O desenvolvimento deste projeto permitiu praticar a organização de informações em planilhas, a utilização de validações de dados, a construção de fórmulas para consolidação de valores e a documentação de uma solução com foco na experiência do usuário.

Além da aplicação técnica dos recursos do Excel, o projeto demonstra como a estruturação de informações pode contribuir para tornar atividades administrativas mais organizadas e facilitar a conferência dos dados.

---

**Projeto desenvolvido para fins de estudo e portfólio a partir de um desafio da DIO.**
