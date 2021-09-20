# ecse373_f21_rza3_publisher_package
## Setting up the package<br>
Download the package and setup your system. In a  Linux terminal, enter the following commands<br>
`source devel/setup.bash`<br>
`catkin_make`<br>
`roslaunch navvis_description launch.launch use_xacro:=true use_gui:=false &`<br>
The '&' sends the job to the background<br>
The last command will launch the navvis robot description in rviz without the joint state publisher gui.
It will also use navvis_defn.xacro instead of navvis_defn.urdf which is important because the xacro contains the Velodyne and Hokuyo LIDARs. 
In order to not use the joint state publisher gui, you can omit the `use_gui` argument as the gui is used by default (you can also use `use_gui:=true`).
Even though you should use navvis_defn.xacro and not navvis_defn.urdf to see the description with the Velodyne and Hokuyo LIDARs, you can still use navvis_defn.urf 
(for example, to look at the LIDARS defined as boxes and cylinders), you can omit the `use_xacro` argument as it is false by defualt or you can use `use_xacro:=false`.
