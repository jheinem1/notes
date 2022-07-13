
## App.java
```Java
class App {
    public static void main(String[] args) {
        Point2D p1 = new Point2D(3, 5);
        Point2D p2 = new Point2D(3, 5);
        if(p1.equals(p2))
        System.out.println("Dist is 0.");
        else
        System.out.println("Dist is " +
        p1.distanceTo(p2));
        System.out.println(p1.x());
        System.out.println(p2.theta());
    }
}
```
## Point2D API
```Java
//Initializes a new point (x, y).
Point2D(double x, double y)
//Returns the x-coordinate.
double x()
//Returns the y-coordinate.
double y()
//Returns the polar radius of this point.
double r()
//Returns the angle of this point in
polar coordinates.
double theta()
//Returns the Euclidean distance between this point and that point.
double distanceTo(Point2D that)
```

## Point2D Implementation
(does not matter *how* Point2D is implemented)
```Java
//from Sedgewick and Wayne
public final class Point2D {
    private final double x;
    private final double y;
    public Point2D(double x, double y) {
        this.x = x;
        this.y = y;
    }
    public double x() {
        return x;
    }
    public double y() {
        return y;
    }
    public double r() {
        return Math.sqrt(x*x + y*y);
    }
    public double theta() {
        return Math.atan2(y, x);
    }
    public double distanceTo(Point2D that) {
        double dx = this.x - that.x();
        double dy = this.y - that.y();
        return Math.sqrt(dx*dx + dy*dy);
    }
    @Override
    public boolean equals(Object other) {
        if (other == this) return true;
        if (other == null) return false;
        if (other.getClass() != this.getClass())
        return false;
        Point2D p = (Point2D) other;
        return this.x() == p.x() &&
        this.y() == p.y();
    }
    @Override
    public String toString() {
        return "(" + x + ", " + y + ")";
    }
}
```