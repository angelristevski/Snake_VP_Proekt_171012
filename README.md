# Snake - Проект по Визуелно програмирање
## Ангел Ристевски, број на индекс 171012
### Краток опис на играта
Играта започнува со табла на која има една жолта точка којашто претставува глава на змијата која може да ја движиме со притискање на копчињата горе, долу лево, десно. 
На случајна позиција на таблата има и црвена точка која претставува храна.
Кога позицијата на змијата ќе стане еднаква со позицијата на храната, змијата се зголемува и на случајна позиција се создава нова храна.
Играта се смета за победена ако змијата изеде 20 точки, а се смета за изгубена ако главата на змијата се судри со некој од ѕидовите или со дел од своето тело.
### Имплементација
Во windows form се креираат PictureBox компоненти за мапата на играта (game_map), главата на змијата (zmija), храната (hrana) и листа од PictureBox компоненти за телото на змијата (zmija_delovi).

Се креираат и променливи cord_x и cord_y за насоката на движење на змијата и променлива index во која се чува должината на змијата.

Се додава timer.

Кога се стартува програмата во Form1_Load функцијата се поставуваат почетните вредности на променливите и се стартува timer-от.

Додаваме KeyDown event со кој ја менуваме насоката на движење на змијата.

Креираме функција iscrtaj_zmija што ја зголемува змијата кога ќе изеде храна.

Со секое отчукување на timer-от ја движиме змијата во соодветната насока, проверуваме дали змијата е на иста позиција со храната и проверуваме дали играта е завршена.