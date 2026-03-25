# 🚀 Clean Architecture SaaS Boilerplate

Een robuust, enterprise-ready fundament voor het bouwen van moderne Software-as-a-Service (SaaS) applicaties. Deze boilerplate combineert een **.NET 10 Web API** volgens Clean Architecture-principes met een **Next.js** frontend en een volledige **Docker** infrastructuur.

Dankzij de ingebouwde templating-engine kun je met één commando een compleet nieuw, op maat genaamd project genereren!

## 🛠️ Tech Stack

**Backend**
* **.NET 10** Web API
* **Clean Architecture** (Domain, Application, Infrastructure, API)
* **Entity Framework Core**
* **ASP.NET Core Identity** (met ingebouwde REST API endpoints)
* **PostgreSQL** Database

**Frontend**
* **Next.js** (App Router)
* **TypeScript**
* **Tailwind CSS**

**Infrastructuur**
* **Docker & Docker Compose**
* **pgAdmin** (Database beheer interface)

---

## 🏗️ Projectstructuur (Clean Architecture)

De backend is strikt opgedeeld in lagen om schaalbaarheid en onderhoudbaarheid te garanderen:

* `[ProjectNaam].Domain`: Bevat de kernentiteiten en interfaces. (Geen externe afhankelijkheden).
* `[ProjectNaam].Application`: Bevat de use cases en bedrijfslogica. (Kent alleen Domain).
* `[ProjectNaam].Infrastructure`: Bevat Entity Framework DbContext, Identity en de PostgreSQL connectie.
* `[ProjectNaam].Api`: De toegangspoort (Controllers). Vangt HTTP requests op en stuurt ze door.

---

## ⚙️ Vereisten

Zorg dat de volgende software op je systeem is geïnstalleerd:
* [.NET 10 SDK](https://dotnet.microsoft.com/download)
* [Node.js](https://nodejs.org/) (LTS versie)
* [Docker Desktop](https://www.docker.com/products/docker-desktop)

---

## 🚀 Installatie van de Template

Installeer deze boilerplate lokaal op je computer, zodat je de `.NET CLI` kunt gebruiken om eindeloos nieuwe projecten te genereren.

1. Clone deze repository naar je lokale machine.
2. Open een terminal in de hoofdmap (waar dit README-bestand staat).
3. Voer het volgende commando uit om de template te installeren:

```bash
dotnet new install .
