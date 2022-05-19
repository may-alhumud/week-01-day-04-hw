# واجب اليوم الرابع




![](https://paper-attachments.dropbox.com/s_82E553B437B45C61DC7E8D5A77BA2743BF7C6CD25ADCD27C906820AECDA2D2B6_1650963884632_image.png)
abstract public class Animal {
private String name;

    public Animal(String name) {
        this.name = name;
    }

    abstract public void greets();
}
public class Cat extends Animal{
public Cat(String name) {
super(name);
}

    @Override
    public void greets() {
        System.out.println("Memw");
    }
}
public class Dog extends Animal{
public Dog(String name) {
super(name);
}

    @Override
    public void greets() {
        System.out.println("woof");
    }
    public void greets(Dog another){
        System.out.println("woooof");
    }
}

public class BigDog extends Dog{
public BigDog(String name) {
super(name);
}

    @Override
    public void greets() {
        super.greets();
        System.out.println("Wooow");
    }

    @Override
    public void greets(Dog another) {
        super.greets(another);
        System.out.println("Woooooow");
    }

    public void greets(BigDog another){
        System.out.println("wooooooooow");
    }
}




----------



![](https://paper-attachments.dropbox.com/s_82E553B437B45C61DC7E8D5A77BA2743BF7C6CD25ADCD27C906820AECDA2D2B6_1650963937695_image.png)

interface Movable {
abstract public void moveUp();
abstract public void moveDown();
abstract public void moveLeft();
abstract public void moveRight();

}

public class MovablePoint implements Movable{
int x;
int y;
int xSpeed;
int ySpeed;

    public MovablePoint(int x, int y, int xSpeed, int ySpeed) {
        this.x = x;
        this.y = y;
        this.xSpeed = xSpeed;
        this.ySpeed = ySpeed;
    }

    @Override
    public String toString() {
        return "MovablePoint{" +
                "x=" + x +
                ", y=" + y +
                ", xSpeed=" + xSpeed +
                ", ySpeed=" + ySpeed +
                '}';
    }

    @Override
    public void moveUp() {
        y-=ySpeed;
    }

    @Override
    public void moveDown() {
        y+=ySpeed;
    }

    @Override
    public void moveLeft() {
        x-=xSpeed;
    }

    @Override
    public void moveRight() {
        x+=xSpeed;
    }
}


 

----------

![](https://paper-attachments.dropbox.com/s_82E553B437B45C61DC7E8D5A77BA2743BF7C6CD25ADCD27C906820AECDA2D2B6_1650963859636_image.png)

abstract public class Shape {
protected String color="red";
protected Boolean filled=true;

    public Shape() {
    }

    public Shape(String color, Boolean filled) {
        this.color = color;
        this.filled = filled;
    }

    public String getColor() {
        return color;
    }

    public Boolean isFilled(){

        return filled;
    }

    public void setColor(String color) {
        this.color = color;
    }

    public void setFilled(Boolean filled) {
        this.filled = filled;
    }

    abstract public double getArea();
    abstract public double getPerimeter();

    @Override
     public String toString() {
        return "Shape{" +
                "color='" + color + '\'' +
                ", filled=" + filled +
                '}';
    }
}

public class Circle extends Shape{
protected double radius=1.0;

    public Circle(){

    }

    public Circle(double radius) {
        this.radius = radius;
    }

    public Circle(String color, Boolean filled, double radius) {
        super(color, filled);
        this.radius = radius;
    }

    public double getRadius() {

        return radius;
    }

    public void setRadius(double radius) {

        this.radius = radius;
    }

    @Override
    public double getArea() {
        double Area;
        Area=Math.PI*radius*radius;
        return Area ;
    }

    @Override
    public double getPerimeter() {
        double perimeter;
        perimeter=2*Math.PI*radius;
        return perimeter;
    }

    @Override
    public String toString() {
        return "Circle{" +
                "radius=" + radius +
                ", color='" + color + '\'' +
                ", filled=" + filled +
                '}';
    }
}
public class Rectangle extends Shape{
protected double width=1.0;
protected double length=1.0;

    public Rectangle(){

    }

    public Rectangle(double width, double length) {
        this.width = width;
        this.length = length;
    }

    public Rectangle(String color, Boolean filled) {
        super(color, filled);
        this.width = width;
        this.length = length;
    }

    public double getWidth() {

        return width;
    }

    public double getLength() {

        return length;
    }

    public void setWidth(double width) {

        this.width = width;
    }

    public void setLength(double length) {

        this.length = length;
    }

    @Override
    public double getArea() {
        double Area;
        Area = width * length;
        return Area;
    }

    @Override
    public double getPerimeter() {
        double perimeter;
        perimeter = 2*(length + width);
        return perimeter;
    }

    @Override
    public String toString() {
        return "Rectangle{" +
                "width=" + width +
                ", length=" + length +
                ", color='" + color + '\'' +
                ", filled=" + filled +
                '}';
    }
}
public class Square extends Rectangle{

    public Square(){

    }

    public Square(double side) {
       
        double area = 4*side;
    }

    public Square(double side ,String color, Boolean filled ) {
        super(color, filled);
        side = side;
    }

    public double getSide(){
        double area;
        double side = 0;
        area=4*side;
        return area ;
    }

    public void setSide(double side){
        
        side=side;
    }

    @Override
    public void setWidth(double side) {

        super.setWidth(width);
    }

    @Override
    public void setLength(double side) {

        super.setLength(length);
    }

    @Override
    public String toString() {
        return "Square{" +
                "width=" + width +
                ", length=" + length +
                ", color='" + color + '\'' +
                ", filled=" + filled +
                '}';
    }
}




