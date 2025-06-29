# Chrome DevTools

## Network

Для начала нужно сохранить профиль HAR с контентом, это будет файл `kmept.ru.har`, находящийся в этом же репозитории

Перейдём к проверке

1. Были найдены два ресурса, которые полностью повторяют содержимое друг друга:

![image](./xhr-double.png)

2. Куча запросов к капче с одинаковым response

![image](./captcha.png)

3. Делать запрос для файла js, в котором содержится только `console.log("Hello")` слегка странно, кому могла бы понадобиться такая функция?

![hello_image](./hello-js.png)

4. Эти логотипы даже не отличаются размером, что уж тут говорить про их разрешение в png, стоило бы использовать webp

![logo](./logo.png)

5. Запросы с ответом в 0 bytes

![metrika](./metrika.png)

## Performance

Сохраним trace.json после того как записали его на вкладке Performance

Время от начала навигации до событий:

 - Nav - LCP: 719.37ms
 - Nav - FCP: 369.30ms
 - Nav - DCL: 620.73ms
 - Nav - Load: 1.63s

![perf](./perf.png)

LCP - сообщение о куках

![lcp](./lcp.png)

DOM-элемент параграф <p/>

![dom-lcp](./dom-lcp.png)

Измерить, сколько времени в миллисекундах тратится на разные этапы обработки документа (Loading, Scripting, Rendering, Painting)

Loading - 25ms
Scripting - 696ms
Rendering - 165ms
Painting - 41ms

## Coverage

Скриншот вкладки:

![sources](./coverage.png)

Размер неиспользованного JS:
Размер неиспользованного CSS
