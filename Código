#include <Wire.h>
#include "Adafruit_MPRLS.h"

#define TCA9548A 0x70


#define RESET_PIN  -1  // set to any GPIO pin # to hard-reset on begin()
#define EOC_PIN    -1  // set to any GPIO pin to read end-of-conversion by

Adafruit_MPRLS mpr = Adafruit_MPRLS(RESET_PIN, EOC_PIN);

void TCA9548A_select(uint8_t bus)
{
  Wire.beginTransmission(TCA9548A);  // Función que nos permitirá seleccionar 
  Wire.write(1 << bus);              // el canal I2C del multiplexor
  Wire.endTransmission();
}



void setup() 
{
   Wire.begin();
   Serial.begin(115200);
   delay(1000);

   Serial.println("------ Datos del test de paracaidas ------");
   Serial.println("");
   Serial.println("------------------------------------------");



// Iniciamos el MPLRS del canal 6
TCA9548A_select(6);

  if (! mpr.begin()) 
  {
    Serial.println("Fallo al conectar con el sensor MPRLS (6)");
    while (1) 
    {
      delay(10);
    }
  }

// Iniciamos el MPLRS del canal 7
TCA9548A_select(7);

  if (! mpr.begin()) 
  {
    Serial.println("Fallo al conectar con el sensor MPRLS (7)");
    while (1) 
    {
      delay(10);
    }
  }
delay(1000);
}

















}


void loop() 
{





 

}
