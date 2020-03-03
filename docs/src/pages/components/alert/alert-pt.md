---
title: Componente do React Alert
components: Alert
---

# Alert

<p class="description">Um alerta exibe uma mensagem curta e importante de uma forma que atrai a atenção do usuário sem interromper o que ele estiver fazendo.</p>

**Observação:** Este componente não está documentado nos [guias do Material Design](https://material.io/), mas o Material-UI o suporta.

## Alerta simples

Este alerta oferece quatro níveis de severidade que definem diferentes ícones e cores.

{{"demo": "pages/components/alert/SimpleAlerts.js"}}

## Descrição

Você pode usar o componente `AlertTitle` para exibir um título formatado acima do conteúdo.

{{"demo": "pages/components/alert/DescriptionAlerts.js"}}

## Ações

Um alerta pode conter uma ação, como um botão de fechar ou desfazer. É renderizado depois da mensagem na parte final do alerta.

Se um `onClose` callback é dado e um atributo `action` é passado, um ícone de fechar é exibido. O atributo `action` pode ser usado para fornecer uma ação alternativa, por exemplo usando um Button ou IconButton.

{{"demo": "pages/components/alert/ActionAlerts.js"}}

### Transição

Você pode utilizar um [transition component](/components/transitions/) como `Collapse` para realizar uma transição na aparência do alerta.

{{"demo": "pages/components/alert/TransitionAlerts.js"}}

## Ícones

O atributo `icon` permite que você adicione um ícone no início do componente de alerta. Isto substituirá o ícone padrão de acordo com a gravidade especificada.

Você pode alterar a gravidade padrão para mapeamento de ícones com o atributo `iconMapping`. Isto pode ser definido globalmente utilizando [theme customization](/customization/globals/#default-props).

Definir o atributo ícone como falso removerá o ícone completamente.

{{"demo": "pages/components/alert/IconAlerts.js"}}

## Variantes

Duas variantes adicionais estão disponíveis – delineadas e preenchidas:

### Outlined

{{"demo": "pages/components/alert/OutlinedAlerts.js"}}

### Preenchido

{{"demo": "pages/components/alert/FilledAlerts.js"}}

## Toast

You can use the Snackbar to [display a toast](/components/snackbars/#customized-snackbars) with the Alert.

## Cor

The `color` prop will override the default color for the specified severity.

{{"demo": "pages/components/alert/ColorAlerts.js"}}

## Acessibilidade

(WAI-ARIA: https://www.w3.org/TR/wai-aria-practices/#alert)

When the component is dynamically displayed, the content is automatically announced by most screen readers. At this time, screen readers do not inform users of alerts that are present when the page loads.

Using color to add meaning only provides a visual indication, which will not be conveyed to users of assistive technologies such as screen readers. Ensure that information denoted by the color is either obvious from the content itself (for example the visible text), or is included through alternative means, such as additional hidden text.

Actions must have a tab index of 0 so that they can be reached by keyboard-only users.
