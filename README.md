# Forward Dynamics Training of Robot
 
 - The goal of this project is to implement learning forward dynamics of a 3 link robot which could account for non-newtonian dynamic factors.
 - There is a "real robot" based on an analytical model (accounting for friction and other non linear factors) and the task was to created a forward dynamics model ("fake robot") trained by the "real robot".

 The programmed ROS node fake_robot.py found in the robot_sim package does the following:

 1) Creates a dataset that contains features(current state and action) and labels(state at the next time step).
 2) Trains a fake robot with the dataset from the real robot with a total time of 10 minutes to collect and train data.
 3) Creates a ROS service that responds to the request (torque commands) from a service client from executive node with the estimated state at the next time step.
