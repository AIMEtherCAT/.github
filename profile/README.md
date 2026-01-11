# Welcome to AIM EtherCAT 👋

**A ROS2-Based EtherCAT communication interface for robotics.**

AIM EtherCAT provides a complete, open-source solution for real-time robot control. From high-level ROS 2 integration to low-level firmware and hardware design, our ecosystem is designed to be flexible, configuration-driven, and easy to deploy.

We aim to provide an efficient way to quickly test and verify control algorithms, even if you are not a developer and are totally unfamiliar with coding. 

Since this framework provides ROS2 topic interfaces, you can not only use your custom nodes to do the control, but also use MATLAB Simulink ROS2 Toolbox to write all the control algorithms in the Simulink!

> [!TIP]
> ~~(机械调车再也不是梦，自己画的车就该自己调)~~

## Project Architecture

Our project is divided into three core components that work seamlessly together:

1.  **Master**: A ROS 2 wrapper for SOEM that provides a communication interface.
2.  **Slave**: Custom STM32 firmware/hardware acting as a low-level controller/control command executor.
3.  **Configuration**: A web-based tool to generate configuration files, dynamically setting up the task list for slaves.

## Repo Structure

* [ROS 2 Master Node](https://github.com/AIMEtherCAT/EcatV2_Master)
* [Configuration Generator](https://github.com/AIMEtherCAT/TaskEditor)
* [Hardware Designs](https://github.com/AIMEtherCAT/EasyCAT_Board)
* Slave Board Firmwares
  * [AX58100+H750](https://github.com/AIMEtherCAT/EcatV2_AX58100_H750_Universal)

## Typical Workflow

To build a robot using our communication interface, simply follow this workflow:

1.  **Hardware Setup**: Connect your slave boards and peripherals/devices (RCs, Sensors, Actuators).
2.  **Configuration**: Use the web configuration generator to define your topology (Slaves, SNs) and assign tasks.
3.  **Run**: Launch the ROS 2 Master node. It will automatically configure the slaves based on your YAML definition.

## Contributing

We welcome contributions! Whether it's adding support for new sensors/actuators in the Slave firmware, optimizing the SOEM wrapper, or improving the Web UI.

Contribution guidelines to be updated.

## Contact & Maintainer

* Hang (scyhx9@nottingham.ac.uk)
