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

4)Dodaj nowego użytkownika, wpisując jego adres e-mail.

![image](https://github.com/user-attachments/assets/0179fb23-6d2d-499d-aa33-13318539f0a4)

5)Określ, jakie uprawnienia mają otrzymać:

Administrator (Admin): Pełny dostęp do wszystkich funkcji, łącznie z możliwością nadawania uprawnień innym.
Członek (Member): Może edytować i udostępniać zawartość grupy roboczej, ale nie ma pełnej kontroli administracyjnej.
Dostawca treści (Contributor): Może edytować zawartość (np. raporty i dashboardy), ale nie może zarządzać grupą roboczą ani nadawać uprawnień.
Widzący (Viewer): Może jedynie przeglądać zawartość grupy roboczej, bez możliwości edytowania lub tworzenia nowych zasobów.

Pamiętaj !!! 
Aby nadać dostęp innym użytkownikom do grupy roboczej, musisz mieć rolę Administratora w tej grupie roboczej.

