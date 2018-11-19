<<<<<<< HEAD
#Donkey Car Sombrero 
Custom hat to simplify donkey car hardware. 
=======
# Donkey Sombrero 
A Rasperry Pi hat for the Donkey Car that provides a few helpful features. 

* The power for the Raspberry Pi comes from the RC car battery.
* A single power switch turns on the car and the pi.
* The PWM controller ins included.
* 3 GPIO pins are accessable. 
* 2 LEDS to indicate stasues. 


## Install 
1. Install the part library.
    ```bash
    pip install git+https://github.com/autorope/donkeypart_sombrero.git
    ```

2. Import Sombrero at the top of your manage.py script.
    ```python
    from donkeypart_sombrero import Sombrero
    ```

3. Update your car's mangae.py script to use the Sombrero instead of the 
other steering and throttle actuators. This section should look like this..

    ```python
    sombrero = Sombrero(
        steering_channel=cfg.STEERING_CHANNEL,
        steering_left_pwm=cfg.STEERING_LEFT_PWM,
        steering_right_pwm=cfg.STEERING_RIGHT_PWM,
        throttle_channel=cfg.THROTTLE_CHANNEL,
        throttle_forward_pwm=cfg.THROTTLE_FORWARD_PWM,
        throttle_stop_pwm=THROTTLE_STOPPED_PWM,
        throttle_reverse_pwm=fg.THROTTLE_REVERSE_PWM
    )
    
    V.add(sombrero, inputs=['angle', 'throttle'])
    ```

>>>>>>> origin/master
