sass свойства 

Sass (Syntactically Awesome Style Sheets) — это расширение CSS, которое добавляет такие возможности, как переменные, вложенные правила, миксины, функции и другие полезные инструменты для создания стилей. Вот некоторые основные свойства и функции, которые предлагает Sass:

1. **Переменные**: Позволяют хранить значения, такие как цвета, шрифты и размеры, чтобы их можно было легко переиспользовать.
   ```scss
   $primary-color: #333;
   ```

2. **Вложенные правила**: Позволяют писать CSS в более читабельной форме, группируя селекторы друг внутри друга.
   ```scss
   .nav {
     ul {
       list-style: none;
     }
     li {
       display: inline;
     }
   }
   ```

3. **Миксины**: Позволяют создавать повторно используемые блоки стилей, которые можно вызывать с параметрами.
   ```scss
   @mixin border-radius($radius) {
     -webkit-border-radius: $radius;
     -moz-border-radius: $radius;
     border-radius: $radius;
   }

   .box { 
     @include border-radius(10px); 
   }
   ```

4. **Наследование**: Позволяет одному селектору наследовать стили другого, что помогает избежать дублирования кода.
   ```scss
   .btn {
     padding: 10px;
     border: none;
   }
   .btn-primary {
     @extend .btn;
     background-color: blue;
   }
   ```

5. **Функции**: Sass предоставляет встроенные функции для работы с цветами, математикой и строками, а также позволяет создавать собственные функции.
   ```scss
   $width: 100px;
   .container {
     width: calc($width * 2);
   }
   ```

6. **Циклы и условия**: Позволяют создавать динамические стили, основываясь на логике.
   ```scss
   @for $i from 1 through 3 {
     .item-#{$i} {
       width: 100px * $i;
     }
   }
   ```

Эти возможности делают Sass мощным инструментом для разработки сложных и поддерживаемых стилей.
