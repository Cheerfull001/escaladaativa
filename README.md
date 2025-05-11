# Sistema de Validação de Conflitos na Escala de Equipes

Este sistema foi desenvolvido para validar conflitos entre a Escala de Equipes e o Remanejamento Mensal, garantindo que funcionários não apareçam simultaneamente em ambas as escalas no mesmo mês.

## Principais Funcionalidades

- **Validação Automática**: O sistema identifica automaticamente quando há conflitos entre a escala de equipes semanal e o remanejamento mensal.
- **Filtros Intuitivos**: Possibilidade de filtrar por mês e equipe para facilitar a visualização.
- **Destaque Visual**: Funcionários em conflito são destacados em vermelho.
- **Indicadores de Conflito**: Ícones e mensagens claras indicam onde existem conflitos.
- **Modo Escuro**: Interface com suporte a tema claro/escuro para melhor experiência visual.

## Como Usar

1. Abra o arquivo `index.html` em um navegador moderno.
2. Use o filtro de mês para visualizar a escala de um mês específico.
3. Observe que quando um mês é selecionado:
   - A tabela de remanejamento mostra a equipe designada para remanejamento naquele mês
   - A escala semanal mostra todas as equipes, exceto a que está em remanejamento
   - Os conflitos são destacados em vermelho quando existem

## Lógica de Validação

O sistema implementa a seguinte regra de negócio:
- Funcionários que aparecem no "Remanejamento Mensal" não devem aparecer na "Escala de Equipes" no mesmo mês.
- A equipe em remanejamento em um determinado mês não deve aparecer na escala de trabalho para esse mesmo mês.

## Estrutura de Dados

- **Equipes**: Cada equipe possui um identificador, nome, cor e lista de membros.
- **Escala Semanal**: Contém semana, período, equipe responsável e mês.
- **Remanejamento Mensal**: Associa um mês específico a uma equipe.

## Exemplo de Conflitos

O sistema identifica três conflitos no exemplo:
1. Equipe 2 em abril (aparece tanto na escala semanal quanto no remanejamento)
2. Equipe 4 em julho (mesmo problema)
3. Equipe 3 em outubro (mesmo problema)

## Tecnologias Utilizadas

- HTML5
- CSS3 (com variáveis para temas)
- JavaScript (ES6+)
- Bootstrap 5
- Font Awesome (para ícones)

## Como Hospedar no GitHub Pages

Se você está tendo problemas para hospedar no GitHub Pages, siga estas instruções:

1. Certifique-se de que o arquivo `index.html` esteja na raiz do repositório (não dentro de uma pasta).
2. Verifique se o GitHub Pages está habilitado nas configurações do repositório.
3. Use a branch principal (main ou master) como origem.
4. Aguarde alguns minutos para que o GitHub Pages processe as alterações após o push.
5. Se ainda estiver tendo problemas, verifique o console do navegador (F12) para ver mensagens de erro específicas.

## Instruções de Customização

Para personalizar este sistema:

1. **Alterar Equipes**: Modifique as sections com classe `team-card` para adicionar ou remover equipes.
2. **Alterar Membros**: Edite as listas `<ul>` dentro dos cards de equipe.
3. **Modificar Escalas**: Atualize as tabelas de escala semanal e remanejamento mensal conforme necessário.
4. **Personalizar Cores**: Altere as variáveis CSS no início do arquivo para modificar as cores do tema.