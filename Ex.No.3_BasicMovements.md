# Ex.No: 3  Basic movements in Unity 
### DATE: 08-03-2025                                                                           
### REGISTER NUMBER : 212223040095
### AIM: 
 To learn the basic movements translation,scaling and rotation of game objects through code.
### Procedure:
1. Setup the Scene
2. Open Unity and create a 3D Scene.
3. Add three objects:Cube → Rename to Object1 (for movement),Sphere → Rename to Object2 (for rotation).Capsule → Rename to Object3 (for scaling).
4. Add the Script,Create a C# Script → Name it TransformOperations.cs.
5. Write the code for translation,scaling and rotation,save and close the script
6. Save the script
7. Select any empty GameObject (or create one: GameObject → Create Empty).
8. Attach the TransformOperations script to it.
9. In the Inspector, assign Object1 → Drag the Cube,Object2 → Drag the Sphere.Object3 → Drag the Capsule.
10. Run the Scene Press Play ▶️ in Unity
11. Stop the program.
### Program 
```
using UnityEngine;
public class TransformOperations : MonoBehaviour
{
    public Transform object1; // Object for translation
    public Transform object2; // Object for rotation
    public Transform object3; // Object for scaling

    public float moveSpeed = 2f;  // Speed of translation
    public float rotateSpeed = 50f; // Speed of rotation
    public float scaleSpeed = 0.5f; // Speed of scaling

    void Update()
    {
        // Translate (Move) object1 along the X-axis- Time.deltaTime to make movement smooth across all frame rates
        if (object1 != null)
        {
            object1.position += Vector3.right * moveSpeed * Time.deltaTime;
        }

        // Rotate object2 around the Y-axis
        if (object2 != null)
        {
            object2.Rotate(Vector3.up * rotateSpeed * Time.deltaTime);
        }

        // Scale object3 up and down
        if (object3 != null)
        {
            float scaleChange = Mathf.PingPong(Time.time * scaleSpeed, 1f) + 0.5f; // generates a value that moves back and forth between 0 and length
            object3.localScale = new Vector3(scaleChange, scaleChange, scaleChange);
        }
    }
}
```
### Output:


BEFORE


![{46C73B04-16EE-4109-BF88-EEDB4CA43D28}](https://github.com/user-attachments/assets/6de837e4-afd6-4a4e-822b-9b6bbb041c3a)





![{EB1E7ADD-94B6-47F9-843D-EE5D78ECDAA7}](https://github.com/user-attachments/assets/3e3fc217-6b87-44b1-86a0-a1c5b4f1ed42)



AFTER

![{2C8667E8-A4B3-4820-A93F-002FF862F011}](https://github.com/user-attachments/assets/971ce9a5-f6f2-4d1f-bfb9-9ceaa239b031)





### Result:
Thus the basic movement is learned through scripting


