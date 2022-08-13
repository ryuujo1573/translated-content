---
title: clamp()
slug: Web/CSS/clamp
translation_of: Web/CSS/clamp()
original_slug: Web/CSS/clamp()
---
{{CSSRef}}

[CSS](/ru/docs/Web/CSS)-функция **`clamp()`** задаёт значение в диапазоне между указанными нижней и верхней границами. Функция принимает три аргумента: минимальное значение, предпочитаемое значение и максимально допустимое. Может использоваться везде, где допускается применение {{CSSxRef("&lt;length&gt;")}}, {{CSSxRef("&lt;frequency&gt;")}}, {{CSSxRef("&lt;angle&gt;")}}, {{CSSxRef("&lt;time&gt;")}}, {{CSSxRef("&lt;percentage&gt;")}}, {{CSSxRef("&lt;number&gt;")}}, или {{CSSxRef("&lt;integer&gt;")}}.

`clamp(MIN, VAL, MAX)` вычисляется как `{{CSSxRef("max", "max")}}(MIN, {{CSSxRef("min", "min")}}(VAL, MAX))`

```css
/* свойство: clamp(expression{3}) */
width: clamp(10px, 4em, 80px);
```

В примере выше ширина будет не меньше 10px и не больше 80px. Но если размер одного "em" будет находиться в диапазоне от 2.5px до 20px (в сумме от 10px до 80px), то ширина будет равняться этим 4em.

Давайте предположим, что в примере выше 1em равен 16px:

```css
width: clamp(10px, 4em, 80px);
/* если 1em = 16px, 4em = (16px * 4) = 64px */
width: clamp(10px, 64px, 80px);
/* clamp(MIN, VAL, MAX) вычисляется как max(MIN, min(VAL, MAX))) */
width: max(10px, min(64px, 80px))
width: max(10px, 64px);
width: 64px;
```

## Синтаксис

Функция `clamp()` принимает в качестве аргументов три разделённых запятой выражения, указываемых в порядке: минимальное значение, предпочитаемое значение, максимальное значение.

_Минимальное значение_ – наименьшее значение, являющееся нижней границей диапазона допустимых значений. Если "предпочитаемое" значение меньше "минимального", будет использоваться именно "минимальное".

_Предпочитаемое значение_ – это выражение, чей результат будет использовать до тех пор, пока будет оставаться в пределах допустимого диапазона значений.

_Максимальное значение_ – наибольшее значение, которое будет устанавливаться, если предпочитаемое будет превышать верхнюю границу допустимого диапазона.

Передаваемые значения могут быть математическими функциями (более подробно смотрите на {{CSSxRef("calc")}}), точными значениями, или другими выражениями, такими как {{CSSxRef("attr", "attr()")}}, результатом которых является допустимый тип аргумента (как например {{CSSxRef("&lt;length&gt;")}}), или вложенные {{CSSxRef("min")}} и {{CSSxRef("max")}} функции. Для математических выражений можно использовать сложение, вычитание, умножение и деление без использования функции `calc()`. Также, можно использовать круглые скобки, чтобы задать порядок вычисление.

Можно использовать разные единицы измерения для каждого значения в выражении и разные единицы измерения в любой математической функции, .являющейся частью любого из аргументов.

### Примечания

- Математические выражения, включающие в себя проценты для ширины и высоты колонок таблицы, групп колонок таблицы, строк таблицы, групп строк таблицы и ячеек таблицы и при значении "auto" и при значении "fixed" свойства "table-layout" могут обрабатываться как если бы было задано значение `auto`.
- Допускается вкладывать функции `max()` и `min()` в качестве значений выражений, в этом случае внутренние обрабатываются как простые скобки. Выражения являются полностью математическими выражениями, поэтому вы можете использовать сложения, вычитание, умножение и деление без использования самой функции calc().
- Выражение может быть значениями, объединяющими операторы сложения (+), вычитания (-), умножения (\*) и деления (/) с использованием стандартных правил приоритета операторов. Не забудьте поставить пробелы с каждой стороны от операндов + и -. Операнды в выражении могут иметь любое значение синтаксиса {{CSSxRef ("&lt;length&gt;")}}. Вы можете использовать разные единицы для каждого значения в своём выражении. Вы также можете использовать круглые скобки, чтобы установить порядок вычислений, когда это необходимо.
- Часто вам может понадобиться использовать {{CSSxRef ("min")}} и {{CSSxRef ("max")}} в функции clamp ().

### Formal syntax

{{CSSSyntax}}

## Примеры

### Установка минимального и максимального размера шрифта

`clamp()` позволяет вам установить размер шрифта, который изменяется в зависимости от ширины области видимости, но не уменьшается ниже и не увеличивается выше заданного размера. Она имеет тот же эффект, что и в [Fluid Typography](https://css-tricks.com/snippets/css/fluid-typography/), но в одну строку и без использования медиавыражений.

```css
p { font-size: clamp(1rem, 2.5vw, 1.5rem); }
```

```html
<p>
If 2.5vw is less than 1rem, the font-size will be 1rem.
If 2.5vw is greater than 1.5rem, the font-size will be 1.5rem.
Otherwise, it will be 2.5vw.
</p>
```

{{EmbedLiveSample("Установка_минимального_и_максимального_размера_шрифта", "100%", "300")}}

## Accessibility concerns

TBD

## Specifications

| Specification                                                                | Status                           | Comment             |
| ---------------------------------------------------------------------------- | -------------------------------- | ------------------- |
| {{SpecName("CSS4 Values", "#calc-notation", "clamp()")}} | {{Spec2('CSS4 Values')}} | Initial definition. |

## Browser compatibility

{{Compat}}

## See also

- {{CSSxRef("calc")}}
- {{CSSxRef("max")}}
- {{CSSxRef("min")}}
- [CSS Values](/ru/docs/Learn/CSS/Introduction_to_CSS/Values_and_units)