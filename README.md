# OOP-Project-Easy-Buying-

#Description

Легка Покупку "Easy Buying"

	
Темою нашого преекту є невеликий додаток який дозволяє спланувати покупки у магазинах. Всі ми хочемо на чомусь зекономити але не завжди це у нас виходить, коли ми йдемо до магазину ми плануємо купити певну кількість продуктів, але найчастіше купуємо більше ніж хотілося б. На це йдуть додаткові кошти, що веде за собою їхню нестачу пізніше.
	Ми плануємо написати додаток так, що він допоможе вирішити ці проблеми. До прикладу: ви вибираєте продукти які б хотіли купити і заносете їх до корзини. Потім після завершення вибору ви заходити в корзину, де автоматично підраховується загальна вартість продукті та знаходиться найблищий магазин де можна придбати їх по найдешевшій ціні. Також додаток передбачатиме коригування продуктів, наприклад можна буде обрати продукт певного виробника і програма внесе його у ваш список як виняток і буде враховувати лише цей продукт.   
	Опис додатку не є цілим, адже в процесі розробки можуть виникнути нові ідеї щодо покращення, або проблеми щодо реалізації, тому кінцевий результат може відрізнятись від початкових цілей.

#Authors

1. Должанов Андрій.
2. Кулачок Михайло.
3. Малюга Дмитро.
4. Северінчик Олександра.

#UML – diagram
(https://drive.google.com/file/d/0BxThNddPcxCQU2hqRDFITTRtUWs/view?usp=sharing)

#Sketch Product
(https://drive.google.com/open?id=0BxThNddPcxCQTDhMYndMQTMwUTg)


#The skeleton code:



public class Main {

    public static void main(String[] args) {
	    User User1 = new User("John", "Snow");

        String People = User1.getInfo();
        System.out.println(People);

        Product Prod1 = new Product("Potato", "Podilski Tomato", 45d);

        String ProdRecord = Prod1.getProducts();
        System.out.println(ProdRecord);

        Shop Shop1 = new Shop("Mega Market","Kovalski, 8", 1253d, 345.7d);

        String SRecord = Shop1.getShopRecord();
        System.out.println(SRecord);

        Marker Marker1 = new Marker("Prostokvashino");

        String Mark = Marker1.getNameMarker();
        System.out.println(Mark);

        

    }
}


public class Marker {
    String NameMarker;

    Marker (String NameMarker){
        this.NameMarker = NameMarker;
    }

    public  String getNameMarker(){
        String Mark = "Marker is: " + NameMarker;
        return  Mark;
    }
}



public class User {

    String firstName;
    String lastName;

    User(String firstName, String lastName) {
        this.firstName = firstName;
        this.lastName =lastName;
    }

    public String getInfo() {
        String people = "User Name: " + firstName + " " +lastName;
        return  people;
    }

    }



public class Product {
    String NameProduct;
    String Brand;
    Double Number;

    Product(String NameProducts, String Brand, Double Number){
        this.NameProduct = NameProducts;
        this.Brand = Brand;
        this.Number = Number;
    }

    public String getProducts() {
        String ProdRecord = "First Product: " +NameProduct + ", " + Brand + ", " + Number;
        return  ProdRecord;
    }
}


public class ProductPrice extends Product {
    ProductPrice(String NameProducts, String Brand, Double Number) {
        super(NameProducts, Brand, Number);
    }
    public void Price (Double price){
        System.out.println(price+" grn");
    }
}



public class Shop {
    String SName;
    Double Distance;
    String Address;
    Double TPrice;

    Shop (String SName, String Address, Double Distance, Double TPrice) {
        this.SName = SName;
        this.Address = Address;
        this.Distance = Distance;
        this. TPrice = TPrice;
    }

    public String getShopRecord(){
       String SRecord = "Shop: " + SName + "; " + Address + "; " + Distance + " meters; " + TPrice + " grn.";
        return  SRecord;
    }
}

