# ROS Noetic

rosrun [pkg] [executable]

rosnode list
	list of nodes registered
rosnode info [running node]
	delivers information about the node
	log functionnality
rosnode kill [node name]
	kills the node --> ros::ok()=false
rosnode ping [node name]
	pings the node
rosrun rqt_graph rqt_graph
	creates a graph of nodes
rostopic echo nodename
	
rostopic info nodename
	to see publisher and subscribers of the topic
# Code
Anonymous nodes! ros::init options

	ros::init(argc, argv, "talker", ros::init_options::AnonymousName);
