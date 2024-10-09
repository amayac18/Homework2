#include <iostream>
#include <string>
#include <unordered_map>

using namespace std;

char mostFrequentChar(const string& str) {
  
    unordered_map<char, int> frequencyMap;

   
    for (char ch : str) {
        frequencyMap[ch]++;
    }

    
    char mostFrequent = '\0';
    int maxCount = 0;

    for (const auto& pair : frequencyMap) {
        if (pair.second > maxCount) {
            mostFrequent = pair.first;
            maxCount = pair.second;
        }
    }

    return mostFrequent;
}

int main() {
    string input;

  
    cout << "Enter a string: ";
    getline(cin, input);


    char result = mostFrequentChar(input);


    if (result != '\0') {
        cout << "Most frequent character: " << result << endl;
    } else {
        cout << "Input string is empty." << endl;
    }

    return 0;
}# Homework2
