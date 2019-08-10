# hello-world

Hi!guys!

I love code,it's very funny!!!!


/*异常指程序运行过程中，阻止其正常运行的问题
 * 异常以throwable作为父类，其直接子类有Error和Exception，程序编程通常只关注Exception
 * 
 * ========================
 * 
 * try和catch关键字：
 * 	通过try和catch关键字捕获异常的话，可使后续代码得到执行（一般程序遇到异常会直接中断程序）；
 * 	try语句中，代码的执行顺序由上往下，当需要第一个异常代码时，try中的后续代码不会执行,然后会再catch语句中匹配异常处理方式
 * 	catch语句可以存在多个，匹配异常的顺序也是按由上往下的顺序，所以一般最大的异常Exception放置最后。
 * finally关键字
 * 	指一切异常的统一出口，不管是否产生异常，最终都会执行此代码。
 * 	关于finally与return关键字的优先级，如果try语句中存在return关键字，系统会先匹配finally语句内容再执行return。
 * 
 */

import org.omg.CORBA.PUBLIC_MEMBER;

public class ex {
	public static void main(String[] args) {
		int a=10;
		int b=0;
		try{
			int c=a/b;  //算术异常
			System.out.println(c);
		}catch(ArithmeticException e){
			e.printStackTrace();  //打印异常结果
		}finally {
			System.out.println("程序结束");
		}
	
	}
}
