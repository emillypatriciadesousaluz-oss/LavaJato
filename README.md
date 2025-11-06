# Lava Jato CleanCar Express (Versão Simples)

## Descrição
Projeto Java simples que simula o gerenciamento de um lava jato. Permite registrar clientes, veículos, funcionários, serviços e atendimentos.

## Estrutura
```
LavaJato/
├── main/ -> Classe principal (Main.java)
├── model/ -> Entidades do sistema (Cliente, Veiculo, etc.)
└── service/ -> Interface e regras de negócio
```

## Execução
Compile tudo e rode o programa:

para copilar
```bash
javac model/*.java service/*.java main/*.java
```
para rodar
```bash
java -cp .:model:service:main Main

```

## Conceitos aplicados
- **Herança:** `Cliente` e `Funcionario` herdam de `Pessoa`
- **Classe abstrata:** `Pessoa`
- **Interface:** `GerenciadorAtendimentos`
- **Composição:** `Atendimento` contém `Cliente`, `Veiculo`, `Servico` e `Funcionario`

## Equipe
- Emilly Patricia de Sousa Luz
- Gabriel Angelo de Lima Dias
- Isabela Lanteuil de Miranda Santiago
- Lucas Cardoso de Alecrim
- Maria Mariana Laurentino Duda
- Gustavo Henrique Vasconcelos Alves de Queiroz
