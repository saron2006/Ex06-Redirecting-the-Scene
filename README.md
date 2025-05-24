# Ex06-Redirect the Scene

## Aim:
To Redirecting the scene in the unity engine.

## Algorithm:
Step 1:
To open the unity engine.

Step 2:
Create a new 3D project.

Step 3:
Create plane and name it as ground and create cube and name it as player.

Step 4:
Add WinText in Hierarchy.

Step 5:
Create a C# Script and name it as playercontroller and add the script to player.

Step 6:
Use the R button to change the level2

Step 7
Print the Output and end the program.

## Program:
## DEVELOPED BY: SARON XAVIER A
## REGISTER NUMBER : 212223230197

## CUBE PLAYER:

```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class Coding : MonoBehaviour
{
    Rigidbody rb;
    public GameObject WinText;
    // Start is called before the first frame update
    void Start()
    {
        rb = GetComponent<Rigidbody>();

    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("Level2");
        }

    }
    private void OnTriggerEnter(Collider other)
    {
        if (other.gameObject.tag == "Cube")
        {
            Destroy(other.gameObject);
            WinText.SetActive(true);
        }
    }
}

```
## Output:

![Screenshot 2025-05-20 120148](https://github.com/user-attachments/assets/4ab438d2-58e9-403a-9a25-6547b98095c0)
![Screenshot 2025-05-20 120219](https://github.com/user-attachments/assets/75643a77-b81d-4317-ae98-ddfd037b94b1)
![Screenshot 2025-05-20 120238](https://github.com/user-attachments/assets/8202a544-2772-4bb0-a79a-629931f569ea)



## Result:

Thus, the execution of above C# coding is successfully redirecting the scene in the unity engine.
