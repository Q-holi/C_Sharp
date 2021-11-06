# C_Sharp

### 접근 제한자, 구조체  
1. public (내부 클래스, 외부 클래스, 파생 클래스, 프로젝트)  
2. internal (내부 클래스, 외부 클래스, 파생 클래스)
3. protected (내부 클래스, 파생 클래스)
4. private (내부 클래스)  
5. protected internal (내부클래스, 파생 클래스, 외부 클래스 중에서 사용하는 클래스가 같은 어셈블리 안에 있을 때 접근가능)  

6. struct (클래스와 유사한 구문, 상속 불가능, 인터페이스 구현 불가능)

```cs
class ExStruct
    {
        struct Point //-- 클래스와 유사한 구문, 상속 불가능, 인터페이스 구현 불가능
        {
            public int x;
            public int y;
            
            public Point(int x, int y) //-- 구조테의 생성자는 매개변수를 넣어서 만들어야 한다. 
            {
                this.x = x;
                this.y = y;
            }
        }
        static void Main(string[] args)
        {
            Point p1 = new Point(); //-- 자동으로 생성
            Point p2 = new Point(100, 200); //-- 100과 200으로 초기화로 생성
            Point p;
            p.x = 1;
            p.y = 2;

            Console.WriteLine("{0},{1}", p.x, p.y);
        }
    }//-- 클래스는 참조의 의한 복사 가능,  구조체는 값에 의한 복사를 실행한다. (차이점)
```


