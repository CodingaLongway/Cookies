#include <iostream>
#include <cmath>
#include <iomanip>

int main() {
    double principal, rate, amount;
    int times_compounded;

    // Ask for the principal
    std::cout << "Enter the principal: ";
    std::cin >> principal;

    // Ask for the interest rate
    std::cout << "Enter the interest rate (as a decimal): ";
    std::cin >> rate;

    // Ask for the number of times the interest is compounded
    std::cout << "Enter the number of times the interest is compounded per year: ";
    std::cin >> times_compounded;

    // Calculate the amount after one year
    amount = principal * std::pow(1 + rate / times_compounded, times_compounded);

    // Display the report
    std::cout << std::fixed << std::setprecision(2);
    std::cout << "Principal: $" << principal << std::endl;
    std::cout << "Interest Rate: " << rate * 100 << "%" << std::endl;
    std::cout << "Times Compounded: " << times_compounded << std::endl;
    std::cout << "Amount in savings after one year: $" << amount << std::endl;

    return 0;
}
