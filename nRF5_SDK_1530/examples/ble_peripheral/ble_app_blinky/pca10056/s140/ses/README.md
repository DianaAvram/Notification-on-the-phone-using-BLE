Here is how to test this example: https://infocenter.nordicsemi.com/index.jsp?topic=%2Fcom.nordic.infocenter.sdk5.v15.0.0%2Fble_sdk_app_blinky.html 
What may be very important for integrating this example with external circuits is the pca10056.h file. This file is located under Notification-on-the-phone-using-BLE/nRF5_SDK_1530/components/boards/ and in the first lines of code, it may be noticed that the buttons and LEDs are mapped to specific GPIOs.  
As it may be seen here: https://infocenter.nordicsemi.com/index.jsp?topic=%2Fcom.nordic.infocenter.sdk5.v12.3.0%2Fgroup__nrf__gpio.html&resultof=%22%6e%72%66%5f%67%70%69%6f%5f%70%69%6e%5f%63%6c%65%61%72%22%20, functiions like:
- nrf_gpio_cfg_input(pin_number) or
- nrf_gpio_cfg_output(pin_number)  
May be used to configure new GPIO pins. 
