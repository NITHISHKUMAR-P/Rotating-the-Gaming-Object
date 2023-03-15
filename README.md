# Ex.No:1  Rotating the Gaming Object

## Aim:
To develop a 3D application for rotating the gaming objects in unity.
## Algorithm:
### Step 1:
&emsp;Start
### Step 2:
1. Click File -> Scene -> Select the scene -> Save as-> New folder(Scenes)-> File name (Exp1)
### Step 3:
1. Click Hierarchy -> 3DObject -> Cylinder
2. Hierarchy -> 3DObject -> Capsule
3. Hierarchy -> 3DObject -> Text
4. Hierarchy -> Effects -> Particle system
### Step 4:
1. Create a folder in project and name as Materials
2. Material folder -> Create -> Material (Name: Capsule)
3. Inspector ->Surface Inputs ->BaseMAp (Choose the color)
4. Drag the Cylinder to the plane and release the mouse
### Step 5:
1. Click Hierarchy -> DirectionalLight
2. Inspector -> Change the color to white (255,255,255)
### Step 6:
&emsp;Create a folder name Coding and create a C# file to add the coding in it.
### Step 7:
&emsp;To add our C# Script file to our selected object, click on the C# Script file and drag it to our selected objects in the Hierarchy window nad run the application.
### Step 8:
&emsp;Stop

## Program:
```
// Program created by: Nithishkumar P
// Register number: 212221230070
```
### Rotate object:
```C#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class rotate : MonoBehaviour
{
    [SerializeField] private Vector3 rotation;
    // Start is called before the first frame update
    // Update is called once per frame
    void Update()
    {
        transform.Rotate(rotation * Time.deltaTime);
    }
}
```
### Revolve around object:
```C#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class caps : MonoBehaviour
{
    public float speed;
    public GameObject obj;
    // Start is called before the first frame update
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        transform.RotateAround(obj.transform.position, new Vector3(0,1,0), speed*Time.deltaTime);
    }
}
```
## Output:
![image](./inter.png)

[[https://user-images.githubusercontent.com/93427237/225361956-3992ae57-67ad-4120-ae83-f8ee104f7b04.mp4](https://github.com/NITHISHKUMAR-P/Rotating-the-Gaming-Object/blob/main/my%20first%20-%20scene1%20-%20PC%2C%20Mac%20%26%20Linux%20Standalone%20-%20Unity%202020.3.45f1%20Personal_%20_DX11_%202023-03-16%2002-23-15%20(online-video-cutter.com).mp4)](https://github.com/NITHISHKUMAR-P/Rotating-the-Gaming-Object/blob/main/my%20first%20-%20scene1%20-%20PC%2C%20Mac%20%26%20Linux%20Standalone%20-%20Unity%202020.3.45f1%20Personal_%20_DX11_%202023-03-16%2002-23-15%20(online-video-cutter.com).mp4)


## Result:
Thus a 3D application for rotating the gaming objects in unity is developed successfully.
