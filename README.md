# VHDL_LIFT_CONTROLLER
The elevator control system functions as a finite state machine (FSM). An FSM is characterized by a collection of states, a starting state, and specific inputs that trigger transitions between states. Based on particular inputs, the FSM may shift from one state to another, a process known as a transition.
<p>
The lift is a customized structure representing a lift shaft to which are fixed three “Call” buttons and associated “lift coming” indicators, plus a rack-and-pinion  gear system and motor whereby a simple platform representing the lift cage can be driven up and down. The position of platform is detected by four more switches- one each for “top”, “middle-plus”, “middle-minus” and “bottom”. The two switches which detect the platform in the middle positon are operated by the rack cage, rather than an isolated point on it – only when both ”middleswitches” are closed is the platform properly aligned. The top and bottom position sensing arrangements don’t need this refinement because any “up” movement with the “top” switch active is illegal, as is “down” movement with 
the “bottom” switch active.
  <br>
This model can be powered using +5V and +12V supplies using a 7 pin DIN connector from an outlet. Simple electronics on a printed circuit board in the model base convert and condition input and outputs, such that each switch provides a logic ‘HI’ when open and ‘LO’ when made (but see A.3 below). The platform motor is driven in response to the UP/DOWN “direction” control line when the “/ENABLE” control line is taken ‘LO’. An integrated motor drive IC is used to provide appropriate connection of the +12V and 0V supplies to the motor, and to limit the current. Crude speed control is possible by Pulse Width Modulation of the enable control line. Each floor indicator is driven by an active LO-control line.
</p>
