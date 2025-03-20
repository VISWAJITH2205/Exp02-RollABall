# Exp02-RollABall

## Aim:
To develop a 3D application for rotating the gaming objects in unity.

## Algorithm:

### STEP 1:
Start

### STEP 2:
Click File -> Scene -> Select the scene -> Save as-> New folder(Scenes)-> File name (Expno1)

### STEP 3:
Click Hierarchy -> 3DObject -> Plane
Hierarchy -> 3DObject -> Sphere

### STEP 4:
Create a folder in project and name as Materials
Material folder -> Create -> Material (Name: Cylinder)
Inspector ->Surface Inputs ->BaseMAp (Choose the color)
Drag the Cylinder to the plane and release the mouse

Create a folder in project and name as Materials
Material folder -> Create -> Material (Name: Capsule)
Inspector ->Surface Inputs ->BaseMAp (Choose the color)
Drag the Capsule to the plane and release the mouse

### STEP 5:
Click Hierarchy -> DirectionalLight
Inspector -> Change the color to white (255,255,255)

### STEP 6:
Add Rigid Body

### STEP 7:
Create a folder name Coding and create a C# file to add the coding in it.

### STEP 8:
To add our C# Script file to our selected object, click on the C# Script file and drag it to our selected objects in the Hierarchy window nad run the application.

### STEP 9:
Stop

## Program:
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class EXP2 : MonoBehaviour
{
    public float xForce = 5.0f;
    public float zForce = 5.0f;
    public float yForce = 100.0f;
    // Start is called before the first frame update
    void Start()
    {     
    }
    // Update is called once per frame
    void Update()
    {
        float x = 0.0f, y = 0.0f, z = 0.0f;
        if (Input.GetKey(KeyCode.A))
        {
            x = x - xForce;
        }
        if (Input.GetKey(KeyCode.D))
        {
            x = x + xForce;
        }
        if (Input.GetKey(KeyCode.W))
        {
            z = z - zForce;
        }
        if (Input.GetKey(KeyCode.X))
        {
            z = z + zForce;
        }
        if (Input.GetKeyDown(KeyCode.Space))
        {
            y = yForce;
        }
        GetComponent<Rigidbody>().AddForce(x,y,z);
    }
}

```
## Output:
![Alt text](<Asset/Screenshot 2025-03-16 115705.png>)

## Result:
3D application for rolling the ball in unity is successfully developed....
