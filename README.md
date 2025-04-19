# TestApp - Version Linux

Projet de démonstration C++/Qt pour Linux Desktop.

## Compilation locale

Prérequis :
- Ubuntu 22.04 ou supérieur
- Qt 6.8.3
- CMake 3.22+
- Ninja (optionnel pour accélérer)


git clone https://github.com/<ton-username>/cyber-ribouldingue-test-linux.git
cd cyber-ribouldingue-test-linux
cmake -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build
./build/TestApp

Lancer les tests

cd build
ctest --output-on-failure

GitHub Actions

À chaque push sur main, le dépôt :

    Compile le projet

    Exécute tous les tests

    Produit un zip contenant TestApp

Artifacts téléchargeables sur chaque build réussi.
