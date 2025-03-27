# 📄 APBD_EFCore_CodeFirst

Rozbudowana aplikacja **REST API** stworzona w .NET Core z wykorzystaniem **Entity Framework Core** w podejściu **Code First**. Projekt skupia się na aspektach bezpieczeństwa, autoryzacji oraz dobrej organizacji warstwy logiki biznesowej i dostępu do danych.

## 📂 Zawartość repozytorium

- `Controllers/` – logika obsługi żądań HTTP
- `Models/` – modele danych EF
- `DTOs/` – obiekty transferowe
- `Repositories/`, `Services/` – wzorce Repository + Service
- `Middlewares/` – własny middleware do logowania wyjątków
- `ExtensionMethods/`, `Enums/`, `Context/` – konfiguracja aplikacji i danych
- `Migrations/` – migracje bazy danych EF Core
- `Program.cs` – punkt wejściowy API
- `appsettings.json` – konfiguracja środowiska
- `logs.txt` – plik logowania błędów

## ⚙️ Technologie

- ASP.NET Core Web API
- Entity Framework Core (Code First)
- JWT Authentication
- PBKDF2 + SALT (hashowanie haseł)
- SQL Server / LocalDB

## 🚀 Funkcjonalności

- Rejestracja i logowanie użytkowników
- Odświeżanie access tokena przy użyciu refresh tokena
- Ochrona endpointów przy użyciu JWT
- CRUD dla encji domenowych
- Middleware logujący wyjątki do pliku tekstowego

## ▶️ Jak uruchomić

1. Otwórz projekt w Visual Studio (`CW9.sln`)
2. Przygotuj bazę danych:
```bash
dotnet ef database update
```
3. Skonfiguruj connection string w `appsettings.json`
4. Uruchom projekt (`dotnet run` lub F5)

## 📌 Przykładowe endpointy

- `POST /api/account/login`
- `POST /api/account/register`
- `GET /api/resource` *(wymaga autoryzacji)*

## 👨‍💼 Autor
**Filip Michalski**  
Projekt wykonany w ramach kursu **APBD (Aplikacje Baz Danych)** jako praktyczne zastosowanie wzorców projektowych, bezpieczeństwa oraz architektury REST API.
