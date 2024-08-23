# ROS2_Publisher
Hacer un programa que:
Implemente un nodo publicador con un contador desde 0 avanzando de 1 en .
Implemente un nodo suscriptor que solo reciba numeros multiplos de 7


# 1. Crear el paquete en un src
    ros2 pkg create --build-type ament_python publicador

# 2. Escribir Nodo Publicador
	  publisher_member_function.py

# 3. Escribir Nodo Suscriptor
	  suscriber_member_function.py

# 4. Agregar dependencias en el setup.py
    entry_points={
        'console_scripts': [
            'talkercito = publicador.publisher_member_function:main',
            'listenercito = publicador.subscriber_member_function:main',
        ],
    },
# 5. Construir y ejecutar

  colcon build 
	source install/setup.bash
	
	ros2 run publicador talkercito
  ros2 run publicador listenercito
  
