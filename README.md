Класс JvmComprehension подгружается в ClassLoader
и далее в Linking, после происходит инициализация
класса, где выполняются инициализаторы static
printAll().

1. В стеке JvmComprehension создается фрейм main(),
   в фрейме main() создаётся и иницилизируенся
   переменная i;
2. В куче создается объект Object а в фрейме main()
   создается ссылка o на этот объект;
3. В куче создается объект Integer(2), а в фрейме
   main() создается ссылка ii объект Integer(2);
4. Создается фрейм printAll() и создаются ссылки
   на Object и Integer(2) в куче,;
5. В куче создается объект Integer(700), а в фрейме
   printAll() создается ссылка uselessVar;
6. Создается новый фрейм куда передаются ссылки на
   Object и Integer, а так же i;
7. Создается опять новый фрейм, куда передается
   строка "finished";
   Garbage Collection ничего не удалял, т.к. ссылки
   на объекты не удалялись.