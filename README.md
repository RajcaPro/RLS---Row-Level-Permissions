# RLS---Row-Level-Permissions
----------
W dzisiejszym wpisie przyjrzymy się dwóm ważnym aspektom zarządzania dostępami: nadawaniu dostępu do pojedynczego raportu oraz do grupy roboczej (workspace).
Omówimy również różnice między tymi dwoma sposobami oraz wymagane uprawnienia potrzebne do nadawania takich dostępów.

Zacznijmy od zadania sobie najważniejszego pytania, jaką wysokie uprawnienia w grupie roboczej musze posiadać aby móc nadawać przypisania/role innym użytkownikom?
Odpowiedź jest prosta:  aby nadawać dostęp do grupy roboczej innym użytkownikom, musisz mieć rolę "Administratora" w tej grupie roboczej.
To kluczowy moment, ponieważ bez tej roli nie będziemy nawet widzieć opcji do sekcji nadawania uprawnień.

Jest jeszcze jedna kluczowa rzecz! :

Aby mieć rolę Administratora grupy roboczej w Power BI, użytkownik musi mieć subskrypcję Power BI Pro lub korzystać z Power BI Premium.

Jeśli grupa robocza jest ustawiona na korzystanie z Power BI Premium, Administrator grupy roboczej musi mieć licencję Pro, aby zarządzać członkami i dostępem, ale inni użytkownicy mogą mieć dostęp do zawartości bez posiadania licencji Pro, o ile są w grupie roboczej.

Ale nie martwcie się! Użytkownicy, którzy korzystają z wersji próbnej Power BI Pro, również mogą pełnić rolę Administratora grupy roboczej. Przynajmniej przez jakiś czas ;D 

--------------------

Teraz możemy przejść do daleszej części i omówić po krótce dostępne role oraz ich możliwości.

Dostępne role w grupie roboczej:

Administrator (Admin): Pełna kontrola nad grupą roboczą. Może zarządzać użytkownikami i ich uprawnieniami, edytować i usuwać zasoby.

Członek (Member): Może tworzyć, edytować i usuwać raporty, ale nie ma dostępu do zarządzania użytkownikami.

Dostawca treści (Contributor): Może edytować raporty i zestawy danych, ale nie ma dostępu do zarządzania grupą.

Widzący (Viewer): Może tylko przeglądać raporty i inne zasoby, bez możliwości edycji.


-----------

Z powyższą wiedzą możemuy już zająć się nadawaniem uprawnień do grupy roboczej !!!

Kroki, aby nadać dostęp do grupy roboczej:

1) Zaloguj się do Power BI Service.

2) Przejdź do grupy roboczej, do której chcesz nadać dostęp.

![image](https://github.com/user-attachments/assets/3e788f9a-ad0c-43cb-bb6a-e6af13fa0cd2)

3) Kliknij ikonę Zarządzaj użytkownikami lub Członkowie (Members).

![image](https://github.com/user-attachments/assets/cc65af7b-c318-4768-ad6f-1acd0d7e798d)

4) Dodaj nowego użytkownika, wpisując jego adres e-mail.

![image](https://github.com/user-attachments/assets/0179fb23-6d2d-499d-aa33-13318539f0a4)

5) Określ, jakie uprawnienia mają otrzymać:

Administrator (Admin): Pełny dostęp do wszystkich funkcji, łącznie z możliwością nadawania uprawnień innym.
Członek (Member): Może edytować i udostępniać zawartość grupy roboczej, ale nie ma pełnej kontroli administracyjnej.
Dostawca treści (Contributor): Może edytować zawartość (np. raporty i dashboardy), ale nie może zarządzać grupą roboczą ani nadawać uprawnień.
Widzący (Viewer): Może jedynie przeglądać zawartość grupy roboczej, bez możliwości edytowania lub tworzenia nowych zasobów.

Pamiętaj !!! 
Aby nadać dostęp innym użytkownikom do grupy roboczej, musisz mieć rolę Administratora w tej grupie roboczej.



-----------------

Super! teraz wiemy jak dodawać użytkowników do grupy roboczej !!!

A co jeśli nie chcemy aby użytkownim miał do niej dostęp tylko mógł przeglądać jeden raport ?
Jest na to rozwiązanie :) 

Kroki, aby nadać dostęp do raportu:

1) Zaloguj się do Power BI Service.

2) Przejdź do raportu, który chcesz udostępnić.

![image](https://github.com/user-attachments/assets/6eb77676-c0d2-471c-8db4-1887a2919fc2)

3) Kliknij przycisk Udostępnij.

4) Wprowadź adres e-mail użytkownika lub grupy, której chcesz nadać dostęp.

![image](https://github.com/user-attachments/assets/f79b9ff2-fed8-4a4f-b771-fcb01098b256)

5) Określ poziom dostępu: możliwość wyświetlania (view) raportu lub dodatkowe opcje, jak edytowanie (edit), jeśli są dostępne.

![image](https://github.com/user-attachments/assets/d4af1da7-69e2-41a6-9793-9cd720c1d8dc)

(Opcjonalnie) Możesz dodać wiadomość i wysłać powiadomienie do użytkownika !!!

Dostępne uprawnienia dla raportu:

View (Wyświetlanie): Użytkownik ma prawo tylko do przeglądania raportu, nie ma możliwości edycji.

Reshare (Ponowne udostępnianie): Umożliwia udostępnianie raportu innym użytkownikom, jeśli taka opcja jest włączona.

Build (Tworzenie na bazie datasetu): Użytkownicy z tym uprawnieniem mogą tworzyć nowe raporty na bazie datasetu z tego raportu.

Aby udostępniać raporty innym użytkownikom, musisz posiadać jedno z poniższych uprawnień:

- Właściciel raportu 

- Administrator grupy roboczej, w której raport się znajduje

- Członek grupy roboczej z uprawnieniem do edycji raportów.


---------------

Przejdźmy do ostatniego kroku czyli nadawanie uprawnień na poziomie wiersza.

Wyobraźmy sobie, że w naszej firmie mamy kilku dyrektorów sprzedaży i każdy z nich ma przypisaną swoją sieć sklepów.
Naszym głównym założeniem jest zablokowanie raportu dla dyrektora sprzedaży, który wybrał złą sieć sklepów (czyli taką którą się nie zajmuje).
Nie chcemy aby miał dostęp do nie swoich danych. 
Kolejnym założeniem jest fakt że Prezes ma mieć dostęp do wszystkich danych czyli wszystkich sieci sklepów, tak aby mógł kontrolować wyniki dyrektorów sprzedaży.

Wydaje się troche skomplikowane prawda ? 
Zapewniam, że po tym wpisie wszystko stanie się jasne :) !

Aby nadać dostęp do grupy roboczej czy wybranego raportu musieliśmy pracować w app powerbi.
Aby dodać uprawnienia na poziomie wiersza musimy działać z poziomu Power BI DESKTOP. !!!!

Zaczynajmy ! 

W pierszym korku kierujemy się do Model View :

![image](https://github.com/user-attachments/assets/de7f3171-01ec-4c3a-8d1d-19973cff1524)

Następnie w prawym panelu strony wybieramy sekcje MODEL.

![image](https://github.com/user-attachments/assets/83fcbef5-7ab7-4809-8f79-7d99aa25a87f)

Szukamy sekcji Roles i klikamy Manage roles.

![image](https://github.com/user-attachments/assets/9762bddb-d6c7-4b23-935e-24162cfafcb6)

Result

![image](https://github.com/user-attachments/assets/d513e814-da37-4d03-ab1d-82e67234c93b)

Dodajemy nową rolę i nazywamy ją XXX :

![image](https://github.com/user-attachments/assets/b8bcdd07-9558-4883-9f9b-6f9c7b988a68)

Wybieramy tabelę na której będą działać uprawnienia oraz poziom nadawania uprawnień w naszym przypadku będzie to imie i nazwisko dyrektora sprzedaży.


![image](https://github.com/user-attachments/assets/e32d6cc5-ce97-4867-8909-0fc191a4059c)


![image](https://github.com/user-attachments/assets/2185fe19-fa71-49ee-8f78-babc583a3f95)

Wybieramy aby kolumna Imie i nazwisko  była równa nazwisku naszego dyrektora.

![image](https://github.com/user-attachments/assets/7ca027ee-9e33-4da3-8089-dc96fee7096b)

teraz gdy już to zrobiliśmy zostaje tylko jedno zadanie !!!

Wracamy do app powerbi do swojej grupy roboczej i wybieramy źródło danych swojego raportu.

![image](https://github.com/user-attachments/assets/7592286a-d9db-447a-93a3-e9de214d51d5)

W tewj sekcji możemy zobaczyć liste naszych dyrektorów oraz liste osób które mają dostęp do ich danych !!!

![image](https://github.com/user-attachments/assets/91ca0811-615c-4cf9-81be-d0cbb920dd8b)





That’s the end of this post!

I hope you will use it in your work 🚀

Best Regards, Mateusz Rajca







