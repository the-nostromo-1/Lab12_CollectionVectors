/*
 * =====================================================================================
 *
 *    Filename:  main_func.cpp
 *
 *    Description: Function definition file for number_collection()
 *
 *    Created:  12/02/2022 12:30:00
 *
 *    Compiler: clang++
 *
 *    Author: David J Tinley
 *
 *   .Organization: CS1B Lab 12
 *
 * =====================================================================================
 */

#include "main.hpp"

using std::vector;
using std::cout;
using std::cin;
using std::endl;

void number_collection() {

    char user_selection;
    vector<double> user_numbers; // initializing empty vector of doubles
    vector<double>::iterator vec_it; // initializing iterator for vector

    do {
        cout << "Please enter a operation to perform." << endl;
        cout << "'q' to quit, 'a' to add, or 'r' to remove." << endl;
        cin >> user_selection;

        switch(user_selection) {
            case 'q': // quit
                break;

            case 'a': // add
                cout << "Enter a number to add" << std::endl;
                int number_added;
                cin >> number_added;

                user_numbers.push_back(number_added);
                sort(user_numbers.begin(), user_numbers.end());

                cout << "Your current numbers now: ";
                for (size_t i = 0; i < user_numbers.size(); ++i) {
                    cout << user_numbers[i] << " ";
                }

                cout << "\nYour current collection size is now: " << user_numbers.size() << endl;
                break;

            case 'r': // remove
                cout << "Enter a number to remove" << std::endl;
                int number_removed;
                cin >> number_removed;

                vec_it = find(user_numbers.begin(), user_numbers.end(), number_removed);

                if (vec_it != user_numbers.end()) {
                    cout << "Number found at " << vec_it - user_numbers.begin() << endl;
                    user_numbers.erase(vec_it);
                    sort(user_numbers.begin(), user_numbers.end());

                    cout << "Your current numbers now: ";
                    for(size_t i = 0; i < user_numbers.size(); ++i) {
                        cout << user_numbers[i] << " ";
                    }
                } else {
                    cout << "Number not found" << endl;
                    sort(user_numbers.begin(), user_numbers.end());

                    cout << "Your current numbers now: ";
                    for(size_t i = 0; i < user_numbers.size(); ++i) {
                        cout << user_numbers[i] << " ";
                    }
                }

                cout << "\nYour current collection size is now: " << user_numbers.size() << endl;
                break;

            default: // handles invalid selections
                cout << "Invalid operation" << endl;
                break;
        }
    } while(user_selection != 'q');
}
