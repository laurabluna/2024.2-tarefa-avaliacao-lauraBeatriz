# 2024.2 Avaliação do 1o período de Sistemas Operacionais

## Informações gerais
- **Aluna**: Laura Beatriz Luna Maia
- **Objetivo do repositório**: Avaliação do 1o bimestre da Disciplina de sistemas operacionais do curso de TADS do IFRN-CNAT
- **Público alvo**: alunos da disciplina de SO (Sistemas Operacionais) do curso de TADS (Superior em Tecnologia em Análise e Desenvolvimento de Sistemas) no CNAT-IFRN (Instituto Federal de Educação, Ciência e Tecnologia do Rio Grande do Norte - Campus Natal-Central).
- disciplina: **SO** Sistemas Operacionais
- professor: [Leonardo A. Minora](https://github.com/leonardo-minora)

## Avaliação
- **Lembre de fazer o fork deste repositório**
- As questões foram construídas com o auxílio do [copilot](https://copilot.microsoft.com/)

# Questão 1. Introdução a sistemas operacionais

Considere as funções e objetivos principais de um sistema operacional conforme discutido no texto. Explique como um sistema operacional gerencia os recursos de hardware e software de um computador para garantir eficiência e segurança. Em sua resposta, aborde os seguintes pontos:

- Gerenciamento de processos
- Gerenciamento de memória
- Gerenciamento de dispositivos de entrada e saída
- Gerenciamento de arquivos

**Dica**: Pense em exemplos práticos de como o sistema operacional realiza essas tarefas no dia a dia de um usuário.

# Resposta questão 1 
a) Gerenciamento de processos
No hardware, o sistema operacional distribui a capacidade de processamento entre diferentes processos de forma justa, utilizando estratégias como escalonamento e prioridades, para evitar a monopolização de recursos por um único programa. No software, ele cria a ilusão de multitarefa ao alternar rapidamente entre os processos, permitindo ao usuário executar várias aplicações simultaneamente.

b) Gerenciamento de memória
No hardware, o sistema operacional aloca espaços na memória RAM para cada processo em execução e, quando a memória física não é suficiente, utiliza a memória virtual no disco rígido para armazenar temporariamente dados menos usados. 

c) Gerenciamento de dispositivos de entrada e saída
O sistema operacional age como um intermediário entre o hardware e os programas, garantindo que dispositivos como teclado, mouse, impressora e discos funcionem corretamente. Ele utiliza drivers para traduzir os comandos enviados pelos programas para uma linguagem que o hardware compreenda. 

d) Gerenciamento de arquivos
O sistema operacional organiza os dados no disco rígido ou SSD em sistemas de arquivos como NTFS, FAT32 ou EXT4, permitindo a criação, leitura, escrita e exclusão de arquivos. Ele também controla o acesso a esses dados para garantir segurança, impedindo que usuários ou processos não autorizados modifiquem ou leiam informações sensíveis.

# Questão 2. Estrutura de sistemas operacionais

## Texto informativo
### Estrutura de Sistemas Operacionais: Custo de Desenvolvimento e Segurança da Informação

A estrutura de um sistema operacional (SO) é fundamental para determinar tanto o custo de desenvolvimento e manutenção quanto a segurança da informação. Existem várias arquiteturas de SO, como monolítica, microkernel e em camadas, cada uma com suas próprias implicações em termos de custo e segurança.

#### Custo de Desenvolvimento e Manutenção

1. **Arquitetura Monolítica**:
   - **Desenvolvimento**: Geralmente, mais rápida de desenvolver inicialmente, pois todos os componentes do SO são integrados em um único bloco de código.
   - **Manutenção**: Pode ser mais complexa e cara, pois qualquer alteração em um componente pode afetar todo o sistema, exigindo testes extensivos e cuidadosos.

2. **Arquitetura Microkernel**:
   - **Desenvolvimento**: Pode ser mais demorada e cara inicialmente, pois envolve a criação de um núcleo mínimo e a implementação de serviços adicionais como processos separados.
   - **Manutenção**: Mais fácil e menos custosa, já que os componentes são isolados. Atualizações e correções podem ser feitas em módulos específicos sem impactar o núcleo do sistema.

3. **Arquitetura em Camadas**:
   - **Desenvolvimento**: Moderadamente complexa, pois cada camada deve ser bem definida e interagir corretamente com as outras.
   - **Manutenção**: Relativamente fácil, pois problemas podem ser isolados e corrigidos em camadas específicas sem afetar o restante do sistema.

#### Segurança da Informação

1. **Arquitetura Monolítica**:
   - **Segurança**: Pode ser mais vulnerável, pois uma falha em qualquer parte do sistema pode comprometer todo o SO. A integração de todos os componentes em um único bloco de código pode dificultar a implementação de medidas de segurança robustas.

2. **Arquitetura Microkernel**:
   - **Segurança**: Geralmente mais segura, pois isola os serviços em processos separados. Isso limita o impacto de uma falha ou ataque a um único componente, protegendo o núcleo do sistema e outros serviços.

3. **Arquitetura em Camadas**:
   - **Segurança**: Oferece um bom equilíbrio, pois cada camada pode implementar suas próprias medidas de segurança. No entanto, a comunicação entre camadas deve ser cuidadosamente gerenciada para evitar vulnerabilidades.

### Conclusão

A escolha da arquitetura de um sistema operacional tem um impacto significativo tanto no custo de desenvolvimento e manutenção quanto na segurança da informação. Arquiteturas monolíticas podem ser mais rápidas e baratas de desenvolver inicialmente, mas podem acarretar custos de manutenção mais altos e maiores riscos de segurança. Por outro lado, arquiteturas microkernel e em camadas podem exigir um investimento inicial maior, mas oferecem vantagens em termos de manutenção e segurança.

## Questão
Com base no texto sobre a estrutura de sistemas operacionais, analise como as diferentes arquiteturas (monolítica, microkernel e camadas) impactam o custo com a equipe de desenvolvimento e a segurança do sistema operacional. Em sua resposta, considere os seguintes pontos:
- Complexidade de implementação e manutenção
- Necessidade de especialização da equipe
- Potenciais vulnerabilidades de segurança
- Facilidade de atualização e correção de falhas

**Dica:** Utilize exemplos de sistemas operacionais reais que adotam essas arquiteturas para ilustrar sua análise.

# Resposta questão 2
1. Arquitetura Monolítica: Complexidade de implementação e manutenção: Devido à integração de todos os componentes em um único bloco de código, o desenvolvimento inicial tende a ser menos complexo. Porém, a manutenção é mais trabalhosa, já que qualquer alteração em um módulo exige um esforço significativo para evitar impactos em todo o sistema. Necessidade de especialização da equipe: A equipe precisa entender profundamente o sistema como um todo, já que as mudanças em um componente podem afetar outros. Potenciais vulnerabilidades de segurança: Essa arquitetura é mais vulnerável, pois uma falha em um único componente pode comprometer o sistema inteiro. Por exemplo, um erro no driver de um dispositivo pode causar falhas em outros serviços críticos. Facilidade de atualização e correção de falhas: Atualizações são mais complexas, pois exigem testes extensivos para garantir que mudanças em um componente não introduzam novos problemas.
Exemplo: O Linux em suas versões iniciais adotava uma arquitetura monolítica, tornando-o vulnerável a falhas decorrentes de sua integração.

2. Arquitetura Microkernel

Complexidade de implementação e manutenção: Mais complexa e demorada de implementar inicialmente, pois o núcleo é mínimo e muitos serviços são desenvolvidos como processos separados. Entretanto, a manutenção é mais simples, pois falhas em um componente dificilmente afetam outros.
Necessidade de especialização da equipe: A equipe deve ter habilidades específicas para desenvolver e gerenciar processos isolados, mas o foco no núcleo é reduzido, o que facilita o treinamento.
Potenciais vulnerabilidades de segurança: A separação dos serviços aumenta a segurança, já que falhas ou ataques a um componente não afetam diretamente o núcleo ou outros processos.
Facilidade de atualização e correção de falhas: Componentes podem ser atualizados independentemente do núcleo, reduzindo o risco de interrupções.
Exemplo: O sistema operacional MINIX utiliza uma arquitetura microkernel, sendo frequentemente citado por sua robustez em segurança.

3. Arquitetura em Camadas

Complexidade de implementação e manutenção: Moderadamente complexa, já que cada camada deve ser bem definida e interagir corretamente com as outras. Essa modularidade facilita a detecção e correção de falhas.
Necessidade de especialização da equipe: A especialização pode ser dividida por camadas, permitindo que diferentes equipes se concentrem em áreas específicas, como gerenciamento de dispositivos ou interface com o usuário.
Potenciais vulnerabilidades de segurança: A segurança pode ser gerida em cada camada, mas falhas na comunicação entre camadas podem introduzir vulnerabilidades.
Facilidade de atualização e correção de falhas: Atualizações podem ser feitas em camadas específicas, sem afetar o restante do sistema, desde que as interfaces entre as camadas sejam mantidas.
Exemplo: O sistema operacional Windows NT adota uma arquitetura em camadas, equilibrando segurança e facilidade de manutenção.

# Questão 3. Introdução à Segurança de Sistemas Operacionais

## Texto informativo

A segurança de um sistema operacional é um aspecto crucial que visa proteger os recursos do sistema contra acessos não autorizados, ataques maliciosos e falhas. Um sistema operacional seguro deve garantir a integridade, confidencialidade e disponibilidade dos dados e serviços. Para alcançar esses objetivos, várias técnicas e mecanismos são implementados, incluindo:

1. **Controle de Acesso**: Define quem pode acessar o sistema e quais recursos podem ser utilizados. Isso é feito através de autenticação (verificação de identidade) e autorização (permissão de acesso).

2. **Criptografia**: Utilizada para proteger dados em trânsito e em repouso, garantindo que apenas usuários autorizados possam acessar informações sensíveis.

3. **Auditoria e Monitoramento**: Registra atividades do sistema para detectar e responder a comportamentos suspeitos ou anômalos.

4. **Isolamento de Processos**: Garante que os processos sejam executados em ambientes isolados, evitando que um processo comprometa a segurança de outro.

5. **Atualizações e Patches**: Manter o sistema operacional atualizado é essencial para corrigir vulnerabilidades conhecidas e proteger contra novas ameaças.


## Questão

Considerando os mecanismos de segurança discutidos, analise como a implementação de controles de acesso e criptografia pode impactar a performance e a usabilidade de um sistema operacional. Em sua resposta, aborde os seguintes pontos:
- Benefícios e desafios de cada mecanismo
- Impacto na experiência do usuário
- Exemplos de situações onde esses mecanismos são críticos

**Dica:** Pense em como esses mecanismos são aplicados em sistemas operacionais que você utiliza no dia a dia, como Windows, Linux ou macOS.

# Resposta Questão 3
- Criptografia

Benefícios:
Confidencialidade: Protege dados em trânsito e em repouso, tornando-os ilegíveis para intrusos.
Integridade: Permite verificar se os dados foram alterados durante a transmissão.
Autenticação: Pode ser usada para autenticar a origem dos dados.

Desafios:
Performance: A criptografia consome recursos computacionais, podendo afetar a performance do sistema, especialmente em dispositivos com recursos limitados.
Complexidade: A escolha do algoritmo de criptografia e a gestão das chaves são tarefas complexas que exigem conhecimento técnico.
Compatibilidade: A interoperabilidade entre diferentes sistemas criptográficos pode ser um desafio.

Impacto na experiência do usuário: Positivo: Aumenta a segurança das comunicações e dos dados armazenados. Negativo: Pode exigir a instalação de software adicional ou a configuração manual de certificados digitais.

Exemplo: HTTPS: Criptografa a comunicação entre o navegador e o servidor web, protegendo informações sensíveis como senhas e dados de cartão de crédito.

- Controles de Acesso

Benefícios:
Confidencialidade: Protege dados sensíveis de acessos não autorizados
Integridade: Garante que os dados não sejam alterados por usuários não autorizados
Disponibilidade: Impede que usuários maliciosos bloqueiem o acesso a recursos críticos

Desafios:
Performance: A autenticação pode adicionar latência ao acesso a recursos, especialmente em sistemas com muitos usuários
Complexidade: A gestão de permissões e a criação de políticas de acesso podem ser complexas, especialmente em ambientes heterogêneos
Usabilidade: Excesso de controles pode tornar o sistema difícil de usar, exigindo que os usuários memorizem muitas senhas e sigam procedimentos complexos

Impacto na experiência do usuário:
Positivo: Aumento da confiança na segurança dos dados e serviços
Negativo: Pode gerar frustração devido a necessidade de autenticação frequente e restrição de acesso a determinados recursos
Exemplos: Autenticação de dois fatores: Aumenta a segurança, mas exige que o usuário forneça uma segunda forma de autenticação (como um código enviado por SMS)

# Questão 4. Custo de Processamento versus Algoritmo Ótimo de Escalonamento

## Texto informativo

O escalonamento de processos é uma função crítica de um sistema operacional, responsável por determinar a ordem em que os processos são executados pelo processador. O objetivo é maximizar a eficiência do sistema, garantindo que os recursos sejam utilizados de maneira justa e eficaz. No entanto, encontrar o algoritmo de escalonamento ótimo envolve um equilíbrio delicado entre o custo de processamento e a eficiência do escalonamento.

### Custo de Processamento

O custo de processamento refere-se ao tempo e aos recursos necessários para executar um algoritmo de escalonamento. Algoritmos mais complexos podem oferecer melhores resultados em termos de tempo de resposta e utilização do processador, mas também podem exigir mais recursos computacionais para tomar decisões de escalonamento. Isso pode incluir tempo de CPU, memória e outras operações de sistema.

### Algoritmo Ótimo de Escalonamento

Um algoritmo ótimo de escalonamento é aquele que maximiza a eficiência do sistema operacional, minimizando o tempo de espera dos processos, o tempo de resposta e o tempo de retorno. Alguns dos algoritmos de escalonamento mais comuns incluem:

- **First-Come, First-Served (FCFS)**: Simples e fácil de implementar, mas pode levar a longos tempos de espera para processos curtos.
- **Shortest Job Next (SJN)**: Minimiza o tempo médio de espera, mas pode ser difícil de implementar devido à necessidade de prever o tempo de execução dos processos.
- **Round Robin (RR)**: Oferece uma abordagem justa, atribuindo fatias de tempo iguais a todos os processos, mas pode resultar em maior sobrecarga de contexto.
- **Priority Scheduling**: Processos com maior prioridade são executados primeiro, mas pode levar à inanição de processos de baixa prioridade.

## Questão

Considerando os conceitos de custo de processamento e algoritmo ótimo de escalonamento, analise como diferentes algoritmos de escalonamento podem impactar a performance de um sistema operacional em termos de tempo de resposta, tempo de espera e utilização do processador. Em sua resposta, aborde os seguintes pontos:
- Vantagens e desvantagens de pelo menos dois algoritmos de escalonamento
- Impacto do custo de processamento na escolha do algoritmo
- Exemplos de situações onde um algoritmo pode ser preferível a outro

**Dica:** Pense em como esses algoritmos são aplicados em diferentes cenários, como sistemas de tempo real, servidores web e sistemas operacionais de uso geral.

# Resposta questão 4

Priority Scheduling:
Vantagens: Permite priorizar processos importantes, como processos em tempo real.
Desvantagens: Processos de baixa prioridade podem sofrer de inanição se não houver oportunidade de execução. A definição de prioridades pode ser complexa.

Round Robin (RR):
Vantagens: Garante um tempo de resposta razoável para todos os processos e evita a inanição.
Desvantagens: O tempo de resposta pode ser maior do que o SJN para processos curtos, devido ao overhead de troca de contexto.

Overhead de troca de contexto: Algoritmos que realizam muitas trocas de contexto (como o Round Robin com um quantum muito pequeno) podem aumentar o overhead do sistema.

Servidores web: Beneficiam de algoritmos que minimizem o tempo de resposta, como o SJN ou o Round Robin.

# Questão 5. Aplicativo em python vs aplicativos em c

## Questão

Explique o caminho que as instruções seguem desde um aplicativo escrito em Python e um aplicativo escrito em linguagem C até serem executadas pelo hardware. Em sua resposta, considere os seguintes pontos:
- O papel do interpretador no caso do Python
- O processo de compilação no caso do C
- A interação entre o kernel do sistema operacional e os drivers de dispositivo
- A tradução final das instruções para o formato binário (0 e 1) executado pelo hardware

**Dica:** Compare e contraste os dois processos, destacando as principais diferenças e semelhanças na forma como as instruções são processadas e executadas.

# Resposta questão 5

Python: Linguagem Interpretada
a) Papel do interpretador: O código-fonte em Python é interpretado por um programa chamado interpretador Python, como o CPython. Ao executar o programa, o interpretador converte o código Python em um formato intermediário chamado bytecode. Esse bytecode é uma representação mais próxima da máquina, mas ainda não diretamente executável pelo hardware. O interpretador, então, executa o bytecode usando uma máquina virtual Python (PVM), que traduz as instruções para chamadas ao sistema operacional e, eventualmente, ao hardware.

b) Interação com o kernel e drivers: O interpretador realiza chamadas ao kernel do sistema operacional para acessar recursos de hardware, como leitura de arquivos ou alocação de memória. Os drivers de dispositivo, gerenciados pelo kernel, permitem que as solicitações de hardware sejam atendidas, como enviar dados para o disco rígido ou a placa de vídeo.

c) Tradução final para binário
As instruções executadas pelo interpretador, em última instância, são traduzidas pelo kernel do sistema operacional para instruções de máquina (binário) compreensíveis pelo hardware, com a ajuda de drivers e do processador.

2. C 
a) Processo de compilação: O código-fonte em C é submetido a um compilador (como GCC ou Clang), que converte o código diretamente em linguagem de máquina (binário) específica para o processador-alvo. O compilador passa por várias etapas: pré-processamento, análise léxica e sintática, otimizações e geração de código binário executável. O resultado final é um arquivo binário que pode ser executado diretamente pelo sistema operacional, sem a necessidade de um interpretador.

b) Interação com o kernel e drivers: Durante a execução, o programa em C faz chamadas ao kernel do sistema operacional usando APIs ou bibliotecas padrão, como a biblioteca C (glibc). Assim como no caso do Python, o kernel interage com os drivers de dispositivo para acessar hardware específico, como leitura de dados ou envio de comandos à GPU.

c) Tradução final para binária: Como o código já foi compilado para linguagem de máquina, ele é executado diretamente pelo processador. O trabalho do kernel e dos drivers aqui é coordenar o acesso aos dispositivos e recursos compartilhados.
