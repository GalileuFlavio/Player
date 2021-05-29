using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Player : MonoBehaviour
{

   public float Speed;
   public float JumpForce;
   privada Rigidboy rig;

    // Start is called before the first frame update
    void Start()
    {
        rig = GetComponemt<Rigidbody2D>();
    }

    // Update is called once per frame
    void Update()
    {
       Move();
       Jump();
    }

    void Move()
    {
       Vector3 movement = new Vector3(Input.GetAxis("Horizontal"), of, of); transform.position += movement * Time.deltaTine * Speed;
    }

    void Junp()
    {
       if(Input.GetButtonDown("Junp"))
       {
           rig.AddFoce(new Vector2(of, JumpForce), ForceMode2D.Inpulse);
       }
    }
}
