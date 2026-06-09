# DecodeLabs-Intership
// Simulate Temperature and Humidity Sensor Data
float temperature;
float humidity;

void setup() {
  Serial.begin(9600);

  // Random seed
  randomSeed(analogRead(0));

  Serial.println("Temperature\tHumidity");
}

void loop() {

  // Generate simulated values
  temperature = random(200, 401) / 10.0;   // 20.0°C to 40.0°C
  humidity = random(300, 901) / 10.0;      // 30% to 90%

  // Display values
  Serial.print("Temp: ");
  Serial.print(temperature);
  Serial.print(" C\t");

  Serial.print("Humidity: ");
  Serial.print(humidity);
  Serial.println(" %");

  // Simulated logging format
  Serial.print("LOG,");
  Serial.print(temperature);
  Serial.print(",");
  Serial.println(humidity);

  delay(2000);
}
