# previous-homework

#include <iostream>
#include <string>
int main() 
{
    std::cout << "Give me a secret word: " << std::endl;
    std::string secret_word;
    std::cin >> secret_word;

    std::string word;
    std::string status;
    for (int count = 1; count <= 6; count++) {
        if (std::cin.fail())
            break;
            std::string match = ".....";
            std::cout << "Give me a guess: " << std::endl;
            std::cin >> word;
            if (word == secret_word) {
                std::cout << word << std:: endl << "You Win!" << std::endl;
                status = "Win";
                break;
            }
            else {
                for (int length = 0; length <= 4; length++) {
                    if (word[length] == secret_word[length]) {
                        match[length] = word[length];
                    }
                    else {
                        if (word.find(secret_word[length]) != std::string::npos) {
                            //match[word.find(secret_word[length])] = '?';
                            match[length] = '?';
                        }
                    }
                } 
                std::cout << match << std::endl;
            }
    }
// MOOSE HOUSE .O.SE .?.SE
    if (status != "Win") {
        std::cout << "You Lose." << std::endl;
    }

    return 0;
}

git status
