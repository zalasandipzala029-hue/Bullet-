# Bullet-
using UnityEngine;  public class Enemy : MonoBehaviour {     void OnCollisionEnter(Collision c)     {         if (c.gameObject.CompareTag("Bullet"))         {             Destroy(gameObject);         }     } }
