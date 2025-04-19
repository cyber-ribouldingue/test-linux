# Documentation - TestApp (Linux)

Bienvenue dans le dépôt `cyber-ribouldingue-test-linux`.

## Prérequis pour utiliser ce dépôt

- Système : Ubuntu 22.04 LTS ou supérieur
- Outils :
  - CMake >= 3.22
  - Qt 6.8.3
  - Ninja (optionnel mais recommandé)
  - Clang++ (compilateur C++ moderne)

---

## Compilation locale (manuel)

```bash
git clone https://github.com/<ton-username>/cyber-ribouldingue-test-linux.git
cd cyber-ribouldingue-test-linux
cmake -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build
./build/TestApp
