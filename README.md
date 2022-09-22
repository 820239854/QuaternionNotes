---

---

# QuaternionNotes

[TOC]

### 1. 绕轴旋转演示 [演示Package](Packages/RotationStarter.unitypackage)

![image-20220922173403181](Images/image-20220922173403181.png)

```csharp
public class Rot : MonoBehaviour
{
    float angle = 45;
    // Start is called before the first frame update
    void Start()
    {
        Vector3 initialPos = this.transform.position;
        float posx = initialPos.x * Mathf.Cos(angle * Mathf.Deg2Rad) + initialPos.z * Mathf.Sin(angle * Mathf.Deg2Rad);
        float posz = initialPos.x * -Mathf.Sin(angle * Mathf.Deg2Rad) + initialPos.z * Mathf.Cos(angle * Mathf.Deg2Rad);
        this.transform.position = new Vector3(posx, this.transform.position.y, posz);
    }
}
```



### 2. 绕轴旋转路径 [演示Package](Packages/RotationStarter2.unitypackage)

![image-20220922174332886](Images/image-20220922174332886.png)

[绘制运动轨迹]](Packages/RotationStarter2.unitypackage)