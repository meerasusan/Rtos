Our tasks are represented by the three tasks task1(), task2(), and task3(). Each assignment replicates a spinning motor rotating at a specific speed by turning the corresponding motor pins on and off. Context switching is handled by the contextSwitch() function, which also saves the context of the current task and loads the context of the next task.

The initializePorts() function designates the pertinent pins as the motor control's outputs. The initializeTimers() method sets the CTC mode for a 1ms interrupt on Timer0. The ISR(TIMER0_COMPA_vect) interrupt service routine is activated once every 1 millisecond and calls the relevant function for the currently active job.

For AVR-specific registers and interrupts, take note that this example needs the avr/io.h and avr/interrupt.h headers. Make sure the required AVR toolchain and libraries are installed.
