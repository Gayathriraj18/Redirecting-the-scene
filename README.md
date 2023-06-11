# Redirecting-the-scene

## Aim:
To Redirecting the scene in the unity engine.V


## Algorithm:
Step 1:
Open the unity engine.

Step 2:
Create a new plane and create a cube and give color for the cube.

Step 3:
Next create sphere in the orgin and change the z-axis and Give the color for the sphere.

Step 4:
Create a tag for the Sphere and Make the sphere and cube as a Rigidbodies and Make the sphere use Gravity.

tep 5:
Create the C# script file in the Assets and write the Coding for the Redirecting.

Step 6:
Next Create a another new scene named as page2.

Step 7
In File->Build settings and drop the both first scene and page2 scene in the Scenes in build setting.

Step 8:
Click the Build and run button in the Build settings and run the scene.

Step 9:
The Sphere after touching the cube it will disappeared and Press the key [R] the redircting to the new scene that is page2.

# Program:
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine.SceneManagement;
using UnityEngine;


public class cubeprog : MonoBehaviour
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
        if(Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("level2");
        }
        
    }
    public void OnMouseDown()
    {
        Destroy(gameObject);
    }
    private void OnCollisionEnter(Collision collision)
    {
        if(collision.gameObject.tag=="cube")
        {
            Destroy(collision.gameObject);
            WinText.SetActive(true);
        }
    }
}
```

## Program:
  ~~~
using System.Collections;
using System.Collections.Generic;
using UnityEngine.SceneManagement;
using UnityEngine;


public class cubeprog : MonoBehaviour
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
        if(Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("level2");
        }
        
    }
    public void OnMouseDown()
    {
        Destroy(gameObject);
    }
    private void OnCollisionEnter(Collision collision)
    {
        if(collision.gameObject.tag=="cube")
        {
            Destroy(collision.gameObject);
            WinText.SetActive(true);
        }
    }
}
~~~
## Output:
  ![K1](https://github.com/Gayathriraj18/Redirecting-the-scene/assets/94154854/193c4fae-1a62-4813-8c8e-4291e9ddbcfa)
![K2](https://github.com/Gayathriraj18/Redirecting-the-scene/assets/94154854/b64bd073-829b-405b-adbc-41a16d228280)
![K3](https://github.com/Gayathriraj18/Redirecting-the-scene/assets/94154854/f2c8b5c2-c0a8-4c44-9480-e8f85a530eef)


## Result:
  Thus the above C# coding is successfully redirecting the scene in the unity engine.
