# PHYS-Pendulum-Powered-Cart
This repository contains a simulation of a pendulum-powered cart. The simulation models the dynamics of a cart that is powered by the swinging of a pendulum attached to it. The motion of the cart is determined by the motion of the pendulum, which is affected by the force applied to the cart and the pendulum's initial conditions.

## Requirements
1. Python 3
2. numpy
3. scipy
4. matplotlib

## Program Description

This code is a simulation of a pendulum-powered cart. The pendulum cart is modeled as a class called `PendulumCart`. The class has several class variables that define the system, such as the length of the pendulum, the mass of the pendulum and cart, the initial velocities of the pendulum and cart, and the acceleration due to gravity.

The class also has several methods, the most important of which is the `_ode` method. This method takes in the current state of the system (x, dx, theta, dtheta) and the time `t`, and returns the derivatives of the state variables (`dx`, `ddx`, `dtheta`, `ddtheta`). These derivatives are used by the `scipy.integrate.odeint` function to simulate the motion of the pendulum cart.

The `simulate` method of the `PendulumCart` class uses the `scipy.integrate.odeint` function to simulate the motion of the pendulum cart. It takes in the initial state of the system, the time range, and the input force as arguments and returns an array containing the state of the system at each time step.

The `DrawCart` class is used to create an animation of the pendulum cart. It takes in an axis and a cart object as arguments, and it has a `draw` method that takes in the position and angle of the cart and pendulum and updates the animation.

The code then creates an instance of the `PendulumCart` class and sets the length of the pendulum, the mass of the pendulum and cart, the initial velocities of the pendulum and cart, and the acceleration due to gravity.

It then calls the `simulate` method of the `PendulumCart` class, passing in the initial state of the system, the time range and the input force, and assigns the result to a variable `y`.

Finally, it creates an instance of the `DrawCart` class, passing in the axis and cart object, and calls the `draw` method of the `DrawCart` class in a loop to update the animation. The loop is passed the position and angle of the pendulum cart at each time step, as determined by the `y` variable.
