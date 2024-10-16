# Cartesian Controllers on Universal Robots

A minimal setup to get the latest UR driver up and running with the `cartesian_controllers` for a *UR10e* robot.
Use this as a starting point to investigate basic mechanisms and to setup your own use case.

Things to check: 
Is your reverse_ip (computer IP) set correctly? 
Is your custom port on the teach pendant set correctly? 

You can use the below terminal line command to publish the target_frame

ros2 topic pub /target_frame geometry_msgs/msg/PoseStamped "{header: {stamp: {sec: $(date +%s), nanosec: $(date +%N | cut -b1-9)}, frame_id: 'base'}, pose: {position: {x: 1.0, y: 0.5, z: 1.0}, orientation: {x: 0.0, y: 0.0, z: 0.0, w: 1.0}}}"

The target wrench can be published from rqt. 

The Hz is set to 100 in the example, so we'll use that.
