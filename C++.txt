
#include <iostream>
#include <unordered_map>
#include <string>

using namespace std;

int main()
{
    //unordered_map es un contenedor basado en tablas hash, donde los indices pueden ser de
    //cualquier tipo, no solo numeros int
    
    unordered_map<char, int> tablahash;
    string cadena = "Actividad2";
    
    int n = cadena.length();
    
    // Iterar por la cadena y guardar cada valor encontrado en la tabla hash
    // Con el "++" guardamos la cantidad de veces que aparece cada caracter
    
    for (int i = 0; i < n; i++)
    {
        tablahash[cadena[i]]++;
    }
    
    // Imprimir los valores con un range-based loop 
    
    for (auto x : tablahash)
    {
        cout << "El caracter" << " " << x.first << " " << "aparece" << " " << x.second << " ";
        x.second == 1 ? cout << "vez" : cout << "veces";
        cout << endl;
    }
    return 0;
}

