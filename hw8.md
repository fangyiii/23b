### hw8_C110118226

請新增一個CShape的子類別CTriangle，其constructor 共有三個double的參數 a,b,c (為直角三角形的三個邊長)，其面積為0.5*a*b，請寫出CTriangle的類別程式與產生其物件的main 程式(顏色為紅色，a=3, b=4, c=5) 

```
class CShape {
    private String color;

    public CShape(String color) {
        this.color = color;
    }

    public void setColor(String color) {
        this.color = color;
    }

    public String getColor() {
        return color;
    }
}

class CTriangle extends CShape {
    private double a;
    private double b;
    private double c;

    public CTriangle(String color, double a, double b, double c) {
        super(color);
        this.a = a;
        this.b = b;
        this.c = c;
    }

    public double getArea() {
        return 0.5 * a * b;
    }
}

public class Main {
    public static void main(String[] args) {
        CTriangle redTriangle = new CTriangle("红色", 3, 4, 5);
        System.out.println("颜色: " + redTriangle.getColor());
        System.out.println("面积: " + redTriangle.getArea());
    }
}
```
