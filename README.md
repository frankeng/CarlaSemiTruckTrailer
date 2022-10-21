# Carla SemiTruck and Trailer

[video](https://www.youtube.com/watch?v=sq825QASvZ4)

Run it under windows 10 with carla 0.0.13 and unreal 4.26

This version is still under construction!

Problems:

- Some time the truck gets stuck, it looks like it is stuck in the floor)
- Spawning the combination in the world could give problems because I did not take the length into account. So the trailer could be placed on an other vehicle
- Cornering with the tractor,does not take into account that there is a trailer behind the truck, so corner me be cut off.

**At the moment my Carla doe not work any more so I could not test the description below **

**please push if you found some improvement!!**

## Put the files in the right place

The whole directory structure and files nee to be copied in to the root folder of Carla.

## Add the Truck and trailer to the Blueprint Library

You also need to add the vehicle to the Blueprint Library.

As described in the [carla docs](https://carla.readthedocs.io/en/latest/tuto_A_add_vehicle/#import-and-configure-the-vehicle) in the section : 9. Add the vehicle to the Blueprint Library.

**9. Add the vehicle to the Blueprint Library**.

**<u>*Point 4. (below) is important*</u>**!

> 1. In `Content/Carla/Blueprint/Vehicle`, open the `VehicleFactory` file.
> 2. In the **Generate Definitions** tab, double click **Vehicles**.
> 3. In the **Details** panel, expand the **Default Value** section and add a new element to the vehicles array.
> 4. <u>Fill in the **Make** and **Model** of your vehicle. For the truck name de **Make** "DAFxf". And for the trailer name the **Make**: "trailer".</u>
> 5. Fill in the **Class** value with your `BP_<vehicle_name>` file.
> 6. Optionally, provide a set of recommended colors for the vehicle.
Name the "model" an "make" as below in the picture
![image](https://user-images.githubusercontent.com/23728090/197251353-f60eecd0-cc48-4896-9b60-1b6cdce0b01d.png)

> 7. Compile and save.
>
> ![vehicle factory](https://carla.readthedocs.io/en/latest/img/vehicle_factory.png)

## Test the vehicle

### Manual driving

Launch CARLA, open a terminal in `PythonAPI/examples` and run the following command:

```sh
python3 manual_controlSemiTrailer.py -n5
```

Note

Even if you used upper case characters in your make and model, they need to be converted to lower case when passed to the filter.

### Generate traffic

Not sure if the below line is correct. Pease try it.

```sh
python3 generate_trafficsemiTrailer.py 
```

