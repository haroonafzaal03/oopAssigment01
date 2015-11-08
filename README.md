#include<iostream>
#include<conio.h>
using namespace  std;
class  OrderDetail
{
public:

    OrderDetail()
    {
        _Id=0;
        qnty=0;
        cout<<"Default"<<endl;
    }
     OrderDetail(int I,int q)
    {
        setId(I);
        setqnty(q);
        cout<<"overloaded"<<endl;
    }
    void setId(int I)
    {
        _Id=I;
    }
    int getId()
    {
      return _Id;
    }
    void setqnty(int Q)
    {
        qnty=Q;
    }
    int getqnty()
    {
      return qnty;
    }
    void display()
    {
        cout<<_Id<<"__"<<qnty;
    }


private:
    int _Id;
    int qnty;
};
class  Item:OrderDetail
{
public:
    Item()
    {


    }
     Item(int It,int P,string t,string N,string Ds,string up ,string Cr,int I,int Q )
    {
        set_ItemId(It);
        setPrice(P);
        setname(N);
        setupdt(up);
        setdes(Ds);
        setcret(Cr);
        setId(I);
        setqnty(Q);
        settype(t);

    }
    void setcret(string cret)
    {
        cret=cret;
    }
    string getcret()
    {
      return cret;
    }
    void setupdt(string up)
    {
        updt=up;
    }
    string getupdt()
    {
      return updt;
    }
    void setdes(string Dees)
    {
        des=Dees;
    }
    string getdes()
    {
      return des;
    }
    void settype(string Typ)
    {
        type=Typ;
    }
    string gettype()
    {
      return type;
    }
    void setname(string nme)
    {
        name=nme;
    }
    string getname()
    {
      return name;
    }
    void set_ItemId(int ItmId)
    {
        _ItemId=ItmId;
    }
    int getItemId()
    {
      return _ItemId;
    }
    void setPrice(int Prce)
    {
        Price=Prce;
    }
    int getPrice()
    {
      return Price;
    }
    void display()
    {
        cout<<_ItemId<<" "<<Price<<" "<<name<<" "<<des<<" "<<updt<<" "<<cret<<" "<<type;
    }
private:
    int _ItemId;
    int Price;
    string name,des,updt,cret,type;
};
class Order:OrderDetail
{
public:
    Order( string  s,string d,string dt,string pt,string pf,string un ,int I,int q)
    {
        setId(I);
        setqnty(q);
        setstatus(s);
        setdeliveryTo(d);
        setdeliveryTime(dt);
        setPickupTime(pt);
        setPickupForm(pf);
        setUsername(un);

    }
    void setstatus(string stat)
    {
        status=stat;
    }
    string getstatus()
    {
      return status;
    }
    void setUsername(string Usrnme)
    {
        Username=Usrnme;
    }
    string getUsername()
    {
      return Username;
    }

    void setdeliveryTo(string dlvryTo)
    {
        deliveryTo=dlvryTo;
    }
    string getdeliveryTo()
    {
      return deliveryTo;
    }
    void setdeliveryTime(string dlvyTme)
    {
        deliveryTime=dlvyTme;
    }
    string getdeliveryTime()
    {
      return deliveryTime;
    }
    void setPickupTime(string PckupTme)
    {
        PickupTime=PckupTme;
    }
    string getPickupTime()
    {
      return PickupTime;
    }
    void setPickupForm(string PckupFrm)
    {
        PickupForm=PckupFrm;
    }
    string getPickupForm()
    {
      return PickupForm;
    }
    void display()
    {
       cout<<endl<<
        getId()<<endl<<
        getqnty()<<endl<<
        status<<endl<<
        deliveryTo<<endl<<
        deliveryTime<<endl<<
        PickupTime<<endl<<
        PickupForm<<endl<<
        Username;
    }
private:
  string  status,deliveryTo,deliveryTime,PickupTime,PickupForm,Username;
};
int main()
{
//    Item(int ItemId,int Price,string type,string Name,string des,string updt ,string cret,int Id,int qnty )
    OrderDetail oo(11,1);
    oo.setId(11);
    oo.setqnty(111);
    oo.display();
    Order OD("ddd","aaa","aaaaa","aaa","aa","aaa",22,23);
    OD.setstatus("lol");
    OD.display();

    getch();
    return 0;
}
