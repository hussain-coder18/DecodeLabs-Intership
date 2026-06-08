# DecodeLabs-Intership
hi
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int i;
    float temperature;

    // Initialize random number generator
    srand(time(0));

    printf("Sensor Data Collection Simulation\n");
    printf("---------------------------------\n");

    // Collect 10 sensor readings
    for(i = 1; i <= 10; i++) {

        // Generate temperature between 20°C and 40°C
        temperature = 20 + (rand() % 21);

        printf("Reading %d : Temperature = %.2f °C\n",
               i, temperature);
    }

    return 0;
}
