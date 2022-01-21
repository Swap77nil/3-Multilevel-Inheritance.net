# personaldetails.net2

using System;

namespace Exercises
{
    class Personaldetails
    {
        string name;
        int age;
        string gender;
        public Personaldetails(string name, int age, string gender)
        {
            this.name = name;
            this.age = age;
            this.gender = gender;
        }
        public virtual void Display()
        {
            Console.WriteLine("\n......PERSONAL DETAILS......\n");
            Console.WriteLine("Name       :"+name);
            Console.WriteLine("Age       :" + age);
            Console.WriteLine("Gender       :" + gender);
        }
    }

    class Coursedetails:Personaldetails
    {
        int regNo;
        string course;
        int semester;
        public Coursedetails(string name,int age,string gender,int regNo,string course,int semester):base(name,age,gender)
        {
            this.regNo = regNo;
            this.course = course;
            this.semester = semester;
        }
        public override void Display()
        {
            base.Display();
            Console.WriteLine("\n......COURSE DETAILS......\n");
            Console.WriteLine("Register Number       :" + regNo);
            Console.WriteLine("Course      :" + course);
            Console.WriteLine("Semester       :" + semester);
        }
    }
    class Markdetails:Coursedetails

}
