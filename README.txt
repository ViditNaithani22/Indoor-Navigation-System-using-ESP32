# Indoor-Navigation-System-using-ESP32
An indoor navigation system created using Arduino and ESP32 module =>

First we need to understand what algorithem is used to convert wifi RSSI to distance.

Distance = 10 ^ ((Measured Power -RSSI)/(10 * N))
Measured Powe r=> is a factory-calibrated, read-only constant that indicates what’s the expected RSSI at a distance of 1 meter to the beacon.

RSSI => received signal strength indicator - The measured signal energy for each received packet is quantized to form the received signal strength indicator (RSSI).
the signal RSSI strength will be around -26 (a few inches) to -100 (40–50 m distance). Due to external factors influencing radio waves — such as absorption, interference, or diffraction — RSSI tends to fluctuate. 

N => Constant depends on the Environmental factor. Range 2–4, low to-high strength. If disturbence in RSSI is low (getting similar RSSI values at a given position) then use 2. If disturbence in RSSI is high (getting completely different RSSI values at a given position) use 4. Otherwise calculate your own N. the meathod is given here - https://journals.sagepub.com/doi/full/10.1155/2014/371350


