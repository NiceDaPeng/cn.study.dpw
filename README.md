/**
Object类里面的toString()方法，
每一个类都默认继承自Object类
Object是所有类的根类。
*/

class Teacher{
	
	String name;
	int age;
	
	//继承了Object类的同toString方法，
	//重写了Object类里面的toString方法
	public String toString(){
			return age+"岁的"+name+"正在教书";
		}
	
}

public class TestObject{
	public static void main(String[] args){
		//System.out.println(args.toString());
		
		Teacher t = new Teacher();
		t.name = "大鹏";
		t.age = 20;
		
		//隐藏调用Object类的toString方法。
		System.out.println(t);
	}
}
