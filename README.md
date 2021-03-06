# grid-honeycombs
## Пример использования:
```html
<div className="grid grid_4 grid_md-12 _align-center-md">
  <div className="col col_2 col_md-12">1</div>
  <div className="col col_2 col_md-12">2</div>
</div>
```
Все переменные в файле _variables.sass
------------
- **$breakpoints**: (sm: 500px, md: 768px, lg: 1024px) !default - брейкпоинты медиа-запросов (sm, md, lg)
- **$media-direction**: 'min' !default - направление медиа-запросов ('min', 'max')
- **$max-columns**: 12 !default - максимальное количество колонок для генерации

## grid-templates
Изменение размера отступов между колонками(gaps) производится в файле `/creators/_grid.sass`  при инициализации гридов в поле   `@include grid-template(gaps)` пример:   `@include grid-template(20px)`

------------
**.grid-MEDIA-COLUMN** - инициализация грид-контейнера
-   MEDIA - тип медиазапроса из $breakpoints (sm, md, lg, etc...)
-   COLUMN - количество колонок для инициализации на данном брейкпоинте из $max-columns

## grid-templates-helpers
**_align-center-MEDIA** - выравнивание грид-компонентов по центру
-   MEDIA - тип медиазапроса из $breakpoints (sm, md, lg, etc...)

**_align-stretch-MEDIA** - грид-компоненты растягиваются таким образом, чтобы занять всё доступное пространство контейнера.
-   MEDIA - тип медиазапроса из $breakpoints (sm, md, lg, etc...)

## grid-cells
**.col-media-COLUMN** - инициализация грид-компонента
-   MEDIA - тип медиазапроса из $breakpoints (sm, md, lg, etc...)
-   COLUMN - количество колонок для заполнения грид-компонентом (максимальное значение в $max-columns)

## grid-cells-helpers
**_align-center-MEDIA** - выравнивание текущего грид-компонента по центру
-   MEDIA - тип медиазапроса из $breakpoints (sm, md, lg, etc...)

**_align-stretch-MEDIA** - текущий грид-компонент растягивается таким образом, чтобы занять всё доступное пространство контейнера.
-   MEDIA - тип медиазапроса из $breakpoints (sm, md, lg, etc...)
