using UnityEngine;

public class GunShoot3D : MonoBehaviour
{
    public GameObject bulletPrefab;
    public Transform firePoint;
    public float speed = 25f;

    void Update()
    {
        if (Input.GetMouseButtonDown(0))
        {
            GameObject b = Instantiate(bulletPrefab, firePoint.position, firePoint.rotation);
            b.GetComponent<Rigidbody>().velocity = firePoint.forward * speed;
            Destroy(b, 2f);
        }
    }
}# Bullet-
using UnityEngine;  public class Enemy : MonoBehaviour {     void OnCollisionEnter(Collision c)     {         if (c.gameObject.CompareTag("Bullet"))         {             Destroy(gameObject);         }     } }
