# Стандарты верстки

## Правила именования классов

- Сначала уникальный префикс
- Через дефис от префикса название блока
- Через двойное подчеркивание от блока навзвание элемента
- Через двойное тире название модификатора

Все слова разделяются тире. 

Пример

```css
.b-top-menu
    .b-top-menu__item
    .b-top-menu__item--active
```

## Обращение к элементам DOM дерева в js

Обращаться к элементам в js нужно через классы с префиксом `js`. 

Пример:

```html
<div class="js-tab__click"></div>
```

```javascript
$('.js-tab__click').on('click', function() {
	// Какой то код
});
```

## Структура папок для js


- js/ `Папка для своих скриптов`
⋅⋅* jquery/
- plugins/
- pluginName.js - `плагин`
- init.js `точка инициализации фраимворка или библиотеки`
- script.js `точка сборки всех скриптов, в этом файле идут только подключения других файлов`
	
## Структура папок для less

```  
less/
    styles.less
    partials/
        variables.less
        mixins.less
        helpers.less
        elements.less
        
        pages/
            home.less
            catalog-categories.less
            catalog-category.less
            catalog-detail.less
            
            /home/
                slider.less
            /catalog-categories/
            /catalog-category/
            /catalog-detail/
            
        template/
            header.less
            aside-left.less
            footer.less
            
        либо
            template/
                blocks/
                    header.less
                    header/
                        topmenu.less
                        search.less
                elements/
                    logo.less
```