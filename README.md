/**
Object 下的equals方法  
首先“== ” 基本数据类型比较的是值是否相等
引用数据类型比较的是地址是否相等。
基本数据类型 == 比较的是值相等 ，有默认值
引用数据类型 == 比较的是地址是否相等。默认值位null

Object里面的equals()方法只是为了比较两个对象的地址是否相等，我们一般
在使用的时候都回对它进行重写。
*/

class Teacher{
	String name;
	int age;
	public int sum(int a,int b){
		return a+b;
	}
	public boolean equals(Object obj){
		boolean flag = false;
		if(obj instanceof Teacher){
			Teacher s = (Teacher)obj;
				if(this.age == s.age && this.name != null && s.name != null &&this.name.equals(s.name)){
					flag = true;
				}
		}
		return flag;
		
	}
}

public class TestEquals{
	public static void main(String[] args){
		Teacher t = new Teacher();
		t.name = "大鹏";
		t.age = 20;
		
		Teacher t1 = new Teacher();
		t1.name = "小明";
		t1.age = 21;
		boolean b = t1.equals(t);
		System.out.println(b);

		
	}
}
