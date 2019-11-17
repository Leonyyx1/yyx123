计181杨亚星2018310349
实验四 字符串实验
 
实验目的

掌握字符串String及其方法的使用
掌握异常处理结构


业务要求


内容：利用已学的字符串处理知识编程完成《长恨歌》古诗的整理对齐工作，写出功能函数，并运行。达到如下功能：
 
1. 每7个汉字加入一个标点符号，奇数时加“，”，偶数时加“。”
2. 允许提供输入参数，统计古诗中某个字或词出现的次数
3. 考虑操作中可能出现的异常，在程序中设计异常处理程序

 
输入：

汉皇重色思倾国御宇多年求不得杨家有女初长成养在深闺人未识天生丽质难自弃一朝选在君王侧回眸一笑百媚生六宫粉黛无颜色春寒赐浴华清池温泉水滑洗凝脂侍儿扶起娇无力始是新承恩泽时云鬓花颜金步摇芙蓉帐暖度春宵春宵苦短日高起从此君王不早朝承欢侍宴无闲暇春从春游夜专夜后宫佳丽三千人三千宠爱在一身金屋妆成娇侍夜玉楼宴罢醉和春姊妹弟兄皆列士可怜光采生门户遂令天下父母心不重生男重生女骊宫高处入青云仙乐风飘处处闻缓歌慢舞凝丝竹尽日君王看不足渔阳鼙鼓动地来惊破霓裳羽衣曲九重城阙烟尘生千乘万骑西南行<未完，待续>
输出：

汉皇重色思倾国，御宇多年求不得。
杨家有女初长成，养在深闺人未识。
天生丽质难自弃，一朝选在君王侧。
回眸一笑百媚生，六宫粉黛无颜色。
春寒赐浴华清池，温泉水滑洗凝脂。
侍儿扶起娇无力，始是新承恩泽时。
云鬓花颜金步摇，芙蓉帐暖度春宵。
春宵苦短日高起，从此君王不早朝。
…………


程序代码

package yyx;
public class  gushi
{
public static void main(String[] args)
{
StringBuffer u=new StringBuffer("汉皇重色思倾国御宇多年求不得杨家有女初长成养在深闺人未识天生丽质难自弃一朝选在君王侧回眸一笑百媚生六宫粉黛无颜色春寒赐浴华清池温泉水滑洗凝脂侍儿扶起娇无力始是新承恩泽时云鬓花颜金步摇芙蓉帐暖度春宵春宵苦短日高起从此君王不早朝承欢侍宴无闲暇春从春游夜专夜后宫佳丽三千人三千宠爱在一身金屋妆成娇侍夜玉楼宴罢醉和春姊妹弟兄皆列士可怜光采生门户遂令天下父母心不重生男重生女骊宫高处入青云仙乐风飘处处闻缓歌慢舞凝丝竹尽日君王看不足渔阳鼙鼓动地来惊破霓裳羽衣曲九重城阙烟尘生千乘万骑西南行 ");//创建字符串1
StringBuffer u1=new StringBuffer("杨家有女初长成");
for (int i = 7;i<u.length();i+=8) {
       u.insert(i, "，");
           }
      for (int a = 15;a<u.length();a+=15) {
       u.deleteCharAt(a);
           }
       for (int b = 15;b<u.length();b+=16) {
           u.insert(b, "。");
           }
       for (int c = 16;c<u.length();c+=17) {
           u.insert(c, "\n");
           }
   System.out.println(u);
boolean b=u.toString().contains(u1);
System.out.println("此段是否包含在主文章中:"+b);
System.out.println("包含次数为："+count(u.toString(),u1.toString()));
}

static int count(String s1,String s2)
{
int c=0;
int index=-1;
while((index=s1.indexOf(s2,index))>-1)
{
index+=7;
c++;

}
return c;
}
}



运行截图
  
编程感想
此次实验是关于字符串的使用，难度不是太高，增加了编程经验和对字符串的理解。
