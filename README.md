#include <iostream>
#include <iomanip>

const int COOKIES_PER_BATCH = 48;
const double SUGAR_CUPS_PER_BATCH = 1.5;
const double BUTTER_CUPS_PER_BATCH = 1.0;
const double FLOUR_CUPS_PER_BATCH = 2.75;

void calculate_ingredients(int num_cookies, double &sugar_cups, double &butter_cups, double &flour_cups) {
    double ratio = static_cast<double>(num_cookies) / COOKIES_PER_BATCH;
    sugar_cups = SUGAR_CUPS_PER_BATCH * ratio;
    butter_cups = BUTTER_CUPS_PER_BATCH * ratio;
    flour_cups = FLOUR_CUPS_PER_BATCH * ratio;
}

int main() {
    int num_cookies;
    std::cout << "How many cookies do you want to make? ";
    std::cin >> num_cookies;

    double sugar, butter, flour;
    calculate_ingredients(num_cookies, sugar, butter, flour);

    std::cout << "To make " << num_cookies << " cookies, you will need:\n";
    std::cout << std::fixed << std::setprecision(2);
    std::cout << sugar << " cups of sugar\n";
    std::cout << butter << " cups of butter\n";
    std::cout << flour << " cups of flour\n";

    return 0;
}
