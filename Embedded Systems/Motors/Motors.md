# Motors research:

For a deeper insight on how motors work, and when you should use each type:

1. Motors for Makers (Matthew Scarpino)

## Contents:
    This subcarpet contains information about ESCs (Electronic Speed Controllers), and motors themselves.

    I still don't know the function for the **Robomaster Assistant**. But I included it. I hope it has controllers. As of the writing of this document, V.1.9 is the lattest release. 

## Notation:

| Abbreviation | Meaning          |
|--------------|------------------|
| SC / ESC     | Speed Controller |
| BLDC         | Brushless DC     |
| SWDC         | Series-Wound DC  |
| SHWDC        | Shunt-Wound DC   |
| PMDC         | Permanent Magnet DC |


## Take into account:

### For motors

### For ESC

If you are researching an ESC, add this table to the description:
| State/Parameter | Description | Is Present (Y/N) | Command |
|-----------------|-------------|------------------|---------|
| Auto-cutoff     | Sets the voltage at wich the ESC reduces power due to a low-voltage state.                                  |         |  |
| Brake           | Sets the motor to braking position. The throttle is the minimum to stop rotation (But doesn't stops a load). |         |  |
| Coast           | Let's the motor rotate until stopped by inertia.                                                            |         |  |
| Timing          | Identifies how quickly pulses are deliverd to the BLDC                                                      |         |  |
| Reverse         | Run in reverse direction.                                                                                   |         |  |
| Reverse delay   | The amount of time defore each reverse in direction                                                         |         |  |
| Current limiter | Sets the masimum amount of current that can be deliered to the motor                                        |         |  |
| Switching freq  | Sets the PMW frequency of the motor control signal                                                          |         |  |
| Starting acc    | Dines how quickly the motor should be accelerated during starp-up                                           |         |  |
| Battery type    | Sets the type of battery that supplies power to the ESC                                                     |         |  |


### Tips:
- Never run a motor to it's full pottential constantly.
- For a more responsive throttle, increase *Switching freq*.
- Motors consume more current at start-up, don't force it with a load.


