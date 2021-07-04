# Robot-arm-project
In this project will create and simulate robot arm using robot operating system (ROS). 


ROS you can installed on Ubuntu by using Virtua Box or VMware, also you can using Online website : https://www.theconstructsim.com , For my project i using the website online.
# Start a new project 
After creating an account at: https://www.theconstructsim.com website, Must click on "create new project" As shown in the picture :

<img width="800" alt="image" src="https://user-images.githubusercontent.com/86571348/124393246-30015980-dd02-11eb-8381-1ef404d8dd62.png">

Then as shown in the picture you have start filling the blanks by choosing the version ROS such as melodic which i used, Then Writing the name of your project and description then click "create" . 

![image](https://user-images.githubusercontent.com/86571348/124395254-ba9a8680-dd0b-11eb-9f0d-5a61e5f44839.png)


# Installing the package arduino_robot_arm 
Firstly, Open the "shell web" as shown in picture :

![image](https://user-images.githubusercontent.com/86571348/124395185-60012a80-dd0b-11eb-93e2-3e1622f350cd.png)


Then use the command ($ sudo apt install git) to clone the robot arm package from GitHub by using the path, as shown in the picture :

<img width="800" alt="image" src="https://user-images.githubusercontent.com/86571348/124394368-dd2aa080-dd07-11eb-98f4-5a6eb8e88821.png">

# Install all the dependencies 
To run the packge we need some dependencies like (Movelt, joint state publisher, gazebo ...) so will used this commands : 
 
 $ rosdep install --from-paths src --ignore-src -r -y
 
 $ sudo apt-get install ros-melodic-moveit
 
 $ sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui
 
 $ sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher
 
 $ sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control
  
<img width="800" alt="image" src="https://user-images.githubusercontent.com/86571348/124394992-722e9900-dd0a-11eb-9b0b-56a306a14d6b.png">
<img width="800" alt="image" src="https://user-images.githubusercontent.com/86571348/124395003-7e1a5b00-dd0a-11eb-8b6d-b15539c2cbf7.png">

# Controlling the motors
Now will run the robot arm packge using this command ($ roslaunch robot_arm_pkg check_motors.launch ) the click on graphical tools which will open the window show the simulate arm , as shown in the picture :

<img width="800" alt="image" src="https://user-images.githubusercontent.com/86571348/124395515-43fe8880-dd0d-11eb-9bc8-029a541271ba.png">
<img width="800" alt="image" src="https://user-images.githubusercontent.com/86571348/124395525-52e53b00-dd0d-11eb-99f2-fc1affbcf0de.png">

  
# Controlling the motors in simulation 
This commands will run the arm simulation on RVis and Gazebo 

$ roslaunch robot_arm_pkg check_motors.launch

$ roslaunch robot_arm_pkg check_motors_gazebo.launch

$ rosrun robot_arm_pkg joint_states_to_gazebo.py

As shown in the pictures 

<img width="800" alt="image" src="https://user-images.githubusercontent.com/86571348/124395749-7c529680-dd0e-11eb-8e5f-d5c5f08c90e3.png">

<img width="800" alt="image" src="https://user-images.githubusercontent.com/86571348/124395758-8d9ba300-dd0e-11eb-994e-093a13bf4ffd.png">

<img width="800" alt="image" src="https://user-images.githubusercontent.com/86571348/124395772-a1470980-dd0e-11eb-8754-dd4f8318158a.png">

<img width="800" alt="image" src="https://user-images.githubusercontent.com/86571348/124395809-f08d3a00-dd0e-11eb-95d0-754ca167b6b3.png">

<img width="800" alt="image" src="https://user-images.githubusercontent.com/86571348/124395817-f71bb180-dd0e-11eb-8004-e19e610c4cc2.png">

# Movelt in Rvis 
To define the positioning and movements of the arm will using movelt which is simulate the arm movement in different directions, By Using this command ($ roslaunch moveit_pkg demo.launch), As shown in the pictures : 

<img width="800" alt="image" src="https://user-images.githubusercontent.com/86571348/124396082-38f92780-dd10-11eb-92b2-6065332b8a73.png">

<img width="800" alt="image" src="https://user-images.githubusercontent.com/86571348/124396087-44e4e980-dd10-11eb-9cec-c8ddb1941209.png">




 

