#include <iostream>
#include <string>
using namespace std;

int main() {
    string text;
    int word = 0, vowel = 0, character = 0, space = 0;
    cout << "Enter a text: ";
    getline(cin, text);

    for (int i = 0; i<text.size(); i++) {
        if (text[i] == ' ') {
            space += 1;
        }
        if (text[i] == 'a' || text[i] == 'A' || text[i] == 'e' || text[i] == 'E' || text[i] == 'i' ||
            text[i] == 'I' || text[i] == 'o' || text[i] == 'O' || text[i] == 'u' || text[i] == 'U') {
                vowel += 1;
            }
    }
    if (text.size() == 0) {
        word = 0;
    } else {
        word = space + 1;
    }
    character = text.size() - space;
    cout << "Number of words: " << word << endl;
    cout << "Number of vowels: " << vowel << endl;
    cout << "Number of characters(without spaces): " << character << endl;
    cout << "Number of characters(with spaces): " << text.size() << endl;


    return 0;
}
