# Booking System API Tests (Postman & Newman)

This project contains automated API tests for a simple Booking System.
The tests were created using Postman and executed with Newman.

The goal of this project is to present my API testing skills
and basic automation knowledge as a Junior QA.

---

## Project Scope

The project covers a complete end-to-end booking flow:

- Authentication – create access token
- Create a new booking
- Get booking details
- Update booking data
- Delete booking
- Verify that the booking was deleted
- Negative login scenario (invalid password)

---

## Technologies Used

- Postman
- JavaScript (Postman pm API)
- REST API
- Newman (Postman CLI)

---

## Test Coverage

The project includes the following types of tests:

- HTTP status code validation
- Response body validation
- Data type validation
- Business logic validation
- Collection variables usage (token, booking ID)
- Chained requests
- Negative test scenarios
- Response time validation

---

## Business Logic Validation

Additional business rules are validated:

- Total price must be greater than 0
- Check-in date must be earlier than check-out date

These validations are executed:

- during booking creation (POST request)
- during booking retrieval (GET request)

This helps detect errors early
and confirms that data is stored correctly.

---

## Running Tests in Postman

1. Import the Postman collection.
2. Set the `bookingUrl` collection variable  
   (example: https://restful-booker.herokuapp.com).
3. Run the collection using Postman Collection Runner.

---

## Running Tests with Newman

The tests can also be executed from the command line using Newman.

Example command:
newman run Booking_System_Tests.postman_collection.json

A HTML test report can be generated using:

newman run Booking_System_Tests.postman_collection.json -r html

---

## Notes

- The tested API returns HTTP 200 for invalid login.
- This behavior was handled by validating the error message
  and checking that the token is not returned.

---

## Author

Portfolio project created for a Junior QA position.

# Testy API Systemu Rezerwacji (Postman & Newman)

Projekt zawiera automatyczne testy API dla przykładowego systemu rezerwacji.
Testy zostały przygotowane w Postmanie oraz uruchamiane z poziomu linii
poleceń przy użyciu narzędzia Newman.

Celem projektu jest zaprezentowanie umiejętności testowania API,
podstaw automatyzacji testów oraz świadomego podejścia do testów
na poziomie Junior QA.

---

## Zakres Projektu

Projekt obejmuje kompletny przepływ end-to-end:

- Autoryzację i generowanie tokena
- Tworzenie nowej rezerwacji
- Pobieranie danych rezerwacji
- Aktualizację danych rezerwacji
- Usuwanie rezerwacji
- Weryfikację poprawnego usunięcia danych
- Scenariusz negatywny logowania (błędne dane)

---

## Wykorzystane Technologie

- Postman
- JavaScript (Postman pm API)
- REST API
- Newman (CLI dla Postmana)

---

## Zakres Testów

Projekt zawiera m.in.:

- Walidację kodów odpowiedzi HTTP
- Walidację struktury i danych odpowiedzi
- Sprawdzanie typów danych
- Walidację logiki biznesowej
- Użycie zmiennych kolekcji (token, ID rezerwacji)
- Łączenie zapytań (chained requests)
- Testy negatywne
- Walidację czasu odpowiedzi

---

## Walidacja Logiki Biznesowej

Zaimplementowano testy sprawdzające podstawowe reguły biznesowe:

- Cena rezerwacji musi być większa od 0
- Data zameldowania musi być wcześniejsza niż data wymeldowania

Walidacje te są wykonywane:

- podczas tworzenia rezerwacji (POST)
- podczas pobierania danych rezerwacji (GET)

Pozwala to na wczesne wykrywanie błędów
oraz potwierdzenie poprawności zapisanych danych.

---

## Uruchamianie Testów w Postmanie

1. Zaimportuj kolekcję do Postmana.
2. Ustaw zmienną kolekcji `bookingUrl`
   (np. https://restful-booker.herokuapp.com).
3. Uruchom kolekcję za pomocą Collection Runnera.

---

## Uruchamianie Testów w Newmanie

Testy można również uruchamiać z poziomu linii poleceń
przy użyciu narzędzia Newman.

Przykładowa komenda:

newman run Booking_System_Tests.postman_collection.json

Możliwe jest również wygenerowanie raportu HTML:

newman run Booking_System_Tests.postman_collection.json -r html

---

## Uwagi

- Testowane API zwraca kod HTTP 200 w przypadku niepoprawnego logowania.
- Zostało to świadomie obsłużone poprzez walidację komunikatu błędu
  oraz sprawdzenie braku tokena w odpowiedzi.

---

## Autor

Projekt wykonany jako element portfolio
na stanowisko Junior QA.
