using System.Collections;
using System.Collections.Generic;
using Unity.VisualScripting;
using UnityEngine;

public class HelloWorld : MonoBehaviour
{


     void OnTriggerEnter(Collider other)
    {    
        other.GetComponent<Jump>().jumpStrength = 10;
    }
     void OnTriggerExit(Collider other)
    {
        other.GetComponent<Jump>().jumpStrength = 2;
    }
}

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class TP : MonoBehaviour
{
    public Transform teleportPoint;

     void OnTriggerEnter(Collider other)
    {
        other.transform.position = teleportPoint.position;
    }
}


using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEditor.SceneManagement;

public class SceneChange : MonoBehaviour
{
    public string sceneName;

    void OnTriggerEnter()
    {
        EditorSceneManager.LoadScene(sceneName);
    
    }

}
