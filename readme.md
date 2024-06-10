# Case - Alocação de Professores

<fig>
<img src="\images\Representacao-SistemaAlocaçãoProfessor.jpg" alt="Imagem representativa do processo do Sistema de Alocação de Professores">
    <figcaption> Figura 1 - Representação do processo do Sistema de Alocação de Professores. </figcaption>
</fig>

## Ferramentas
* [Miro](https://miro.com) - Ferramenta utilizada para mapear o processo do Sistema de Alocação de Professores.
* [Draw.io](https://app.diagrams.net/) - Software online para criar os fluxogramas do sistema, tanto o principal quanto o alternativo.

## Introdução

> O case consiste na criação de um épico, as histórias de usuário (HUs) e o seu respectivo fluxo (principal e alternativo) referente ao problema de alocação de professores em cada turma do Ensino Fundamental I de uma escola. Para isso, considere-se as seguintes restrições:
    * **R1 - Restrição de turno**: Os professores só podem ser alocados em séries de um único turno (manhã ou tarde).
    * **R2 - Restrição de qualificação**: Os professores só podem ser alocados em turmas que correspondem às suas áreas de especialização e qualificações educacionais. Os professores da série do primeiro ano somente dão aula para esta série por conta da sua qualificação, uma vez que são responsáveis pelo processo de alfabetização. Portanto, o professor somente poderá lecionar no 1° ano.
    * **R3 - Restrição de quantidade de aulas por semana**: Os professores só podem ser atribuídos a um número máximo de 20 aulas por semana, garantindo que não haja sobrecarga de trabalho e permitindo um tempo adequado para o planejamento e preparação das aulas.

## Épico
Em uma escola municipal do Ensino Fundamental I, há a necessidade de um sistema para alocação de professores às turmas de acordo com suas especializações e restrições de disponibilidade. O objetivo é otimizar a alocação de professores levando em consideração o turno, a qualificação e o limite de aulas por semana.

## Histórias do usuário (HUs):
**História do usuário 1: Cadastrar professor**:
Como diretor(a) e/ou coordenador(a) pedagógico, desejo cadastrar os professores no sistema, especificando suas especializações e disponibilidade de turno (manhã ou tarde), para facilitar a alocação adequada nas turmas.
**Critérios de aceitação**:
1. O sistema deve permitir o cadastro de professores com os seguintes dados obrigatórios: nome completo, especialização e disponibilidade de turno (manhã ou tarde).
2. Ao cadastrar um professor, o sistema deve validar se todos os campos obrigatórios foram preenchidos corretamente.
3. O sistema deve permitir a edição dos dados cadastrados de um professor, incluindo suas especializações e disponibilidade de turno, quando necessário.

***História do usuário 2: Alocar professores conforme restrições**:
Como diretor(a) e/ou coordenador(a) pedagógico da escola, desejo que o sistema aloque automaticamente os professores às turmas do Ensino Fundamental I, de acordo com suas especializações e o turno disponível (manhã ou tarde), respeitando as seguintes restrições:
    1. Os professores devem ser alocados em um único turno (manhã ou tarde).
    2. Cada professor só pode lecionar na série que corresponde à sua área de especialização.
        Por exemplo, um professor especializado em alfabetização só pode lecionar no 1° ano.
    3. Garantir que os professores não ultrapassem o limite de 20 aulas por semana.
**Critérios de aceitação**:
1. O sistema deve permitir alocação automática dos professores de acordo com suas qualificações e disponibilidade de turno.
2. Após a alocação automática, o sistema deve gerar um relatório que detalhe quais professores foram atribuídos a cada turma, levando em consideração as regras de alocação definida.
3. Ao alocar um professor em uma turma, o sistema deve verificar se ele está dentro do limite de 20 aulas por semana.
4. Caso um professor não possa ser alocado devido a restrições, o sistema deve fornecer uma notificação ou sugestão para resolver o problema.

**História do usuário 3: Gerar relatórios de alocação**:
Como diretor(a) e/ou coordenador(a) pedagógico, desejo gerar relatórios detalhados sobre as alocações de professores em cada turma, para acompanhar a distribuição dos recursos educacionais de forma eficiente.
**Critérios de aceitação**:
1. O sistema deve permitir a geração de relatórios detalhados sobre as alocações de professores em cada turma do Ensino Fundamental I.
2. Os relatórios gerados devem incluir informações como o nome do professor, turma atribuída, especialização do professor e turno de disponibilidade.

**História do usuário 4: Tratamento de fluxos alternativos**:
Como diretor(a) e/ou coordenador(a) pedagógico, desejo que o sistema trate fluxos alternativos caso haja restrições ou conflitos durante a alocação dos professores, como:
    1. Um professor estar disponível apenas em um turno específico (manhã ou tarde).
    2. Um professor especializado em uma série específica (por exemplo, 1° ano).
    3. A identificação de professores que já atingiram o limite máximo de aulas semanais.
**Critérios de aceitação**:
    1. O sistema deve ser capaz de lidar com situações em que determinados professores não podem ser alocados devido às restrições.
    2. Deve fornecer alternativas viáveis, como a redistribuição de professores ou a sugestão de novas atribuições.

## Fluxo principal do sistema:
<fig>
<img src="/images/fluxoPrincipal.png" alt="Fluxo principal do sistema.">
    <figcaption>Figura 2 - Representação do fluxo principal do Sistema de Alocação de Professores.</figcaption>
</fig>

1. Receber dados dos professores e turmas:
    * O sistema recebe as informações sobre os professores disponíveis, incluindo suas especializações, disponibilidade de turno e limite máximo de aulas por semana.
    * Também recebe informações sobre as turmas do Ensino Fundamental I que precisam ser alocadas.
2. Verificar disponibilidade e restrições:
    * Para cada turma a ser alocada, o sistema verifica quais professores estão disponíveis no turno correspondente (manhã ou tarde) e possuem a especialização necessária para lecionar na série da turma.
3. Verificar limite máximo de aula:
    * O sistema também verifica se atribuir um professor à turma não excederá o limite máximo de 20 aulas por semana para esses professores.
4. Atribuir professores às turmas:
    * Com base nas verificações anteriores, o sistema atribui automaticamente um professor à turma, considerando todas as restrições.
    * Se houver mais de um professor disponível para uma turma, o sistema pode usar critérios adicionais (como carga horária atual do professor) para tomar a decisão de alocação.
5. O sistema fornece relatórios detalhados sobre a alocação, identificando quaisquer conflitos ou restrições que precisam ser tratados.

## Fluxo alternativo - Conflitos de alocação:
<fig>
<img src="/images/fluxoAlternativo.png" alt="Fluxo alternativo do sistema">
    <figcaption>Figura 3 - Representação do fluxo alternativo do Sistema de Alocação de Professores.</figcaption>
</fig>

1. Identificar conflitos de alocação:
    * Se durante o processo um professor não puder ser atribuído a uma turma devido a restrições (por exemplo, nenhum professor disponível para a série específica), o sistema identifica o conflito.
2. Busca soluções alternativas:
    * O sistema tenta resolver o conflito buscando soluções alternativas, como:
        * Reatribuir outros professores que possam cumprir os critérios.
        * Propor novas alocações que minimizam o impacto das restrições.
        * Notificar os responsáveis para intervenção manual se não houver solução imediata automatizada.
    3. Registrar intervenção manual:
        * Se nenhuma solução automatizada for possível, o sistema registra o conflito e aguarda a intervenção manual.
        * O diretor e/ou coordenador(a) pedagógico podem revisar manualmente as alocações e realizar ajustes conforme necessário, mantendo registros dessas intervenções para análise futura.

<hr>

Kamila Antunes ☕
