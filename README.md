# ol-academy-advanced-js-homeworks
Homework-1
შექმენით Constructor Function სახელად Car, რომელიც იღებს შემდეგ არგუმენტებს:

function Car(make, model, year) {
  // your code goes here...
}
დააიმპლემენტირეთ getCarInfo() მეთოდი რომელიც აბრუნებს ავტომობილის შესახებ ინფორმაციას შემდეგ ფორმატში:

`Tesla Model S released in 2015`
სადაც: Tesla = make, Model S = model და 2015 = year.

შექმენით ახალი Constructor Function სახელად Person, რომელიც მიიღებს შემდეგ არგუმენტებს:

function Person(name, surname, age, gender, cars) {
  // your code goes here...
}
შენიშვნა: cars არგუმენტი გახადეთ optional(არჩევითი) და მისი არ გადმოცემის შემთხვევაში Default value(საწყისი მნიშვნელობად) მიანიჭეთ ცარიელი მასივი [].

Person კონსტრუქტორ ფუნქციაში დააიმპლემენტირეთ fullName და countCars მეთოდები შესაბამისად:

fullName() უნდა აბრუნებდეს სრულ სახელს (name და surname გამოყოფილი space ით)
countCars() უნდა აბრუნებდეს cars მასივში არსებული ელემენტების(მანქანების) რაოდენობას.
დაუბრუნდით Car კონსტრუქტორ ფუნქციას და დაამატეთ ამ კონტექსტში ცვლადი owners საწყისი მნიშვნელობით = [] (ცარიელი მასივი). აღსანიშნავია, რომ owner ცვლადის მნიშვნელობა არ იყოს განსაზღვრული გადმოცემული პარამეტრით (ანუ არ უნდა გადმოეცემოდეს კონსტრუქტორ ფუნქციას).

დააიმპლემენტირეთ Car კონსტრუქტორ ფუნქციაში შემდეგი მეთოდები:

addOwner, რომელიც მიიღებს ერთ პარამეტრს(მფლობელს) და ჩაამატებს კონტექტის ცვლად owners მასივში.
removeOwner, რომელიც მიიღებს ერთ პარამეტრს(მფლობელს) და ამოშლის მას owners მასივიდან.
getOwnersCount, რომელიც დააბრუნებს იმ პირთა რაოდენობას, რომელთაც ეს ავტომობილი ყავთ.
დაუბრუნდით Person კონსტრუქტორ ფუნქციას და დააიმპლემენტირეთ ორი მეთოდი buysCar და sellsCar.

buysCar მეთოდი იღებს ერთ პარამეტრს (ავტომობილს) ამატებს მას კონტექსტის cars მასივში და ამ ავტომობილის მფლობელთა სიაში ამატებს ახალ მფლობელს(მთლიან მიმდინარე Person-ს, თავისი თვისებებით)

sellsCar მეთოდი იღებს ერთ პარამეტრს (ავტომობილს) შლის მას კონტექსტის cars მასივიდან და ასევე ამ ავტომობილის მფლობელთა სიიდან შლის ამ მფლობელს(მთლიან მიმდინარე Person-ს, თავისი თვისებებით)

აღსანიშნავია: ამ გზით ჩვენ ახლა უკვე გვეძლევა საშუალება Cars კონსტრუქტორ ფუნქციიდან გამოვიძახოთ Person კონსტრუქტორ ფუნქციის თვისებები, რადგან ჩვენ Cars ის კონტექსტში ვინახავთ ცვლად owners, რომელიც წარმოადგენს Persons ის instance-ს, რაც თავის მხრივ ნიშნავს, რომ გააჩნია ყველა თვისება რაც მის შემქმნელ კონსტრუქტორ ფუნქციას(ამ შემთხვევაში Person-ს)

დავაიმპლემენტიროთ Car კონსტრუქტორ ფუნქციაში მეთოდი getOwnerNames, რომელიც ამოიკითხავს კონტექსტის owners მასივიდან ყველა მფლობელს და დააბრუნებს მათ სრულ სახელს მათი fullName() ფუნქციის გამოყენებით.

ასევე Car კონსტრუქტორ ფუნქციაში დავაიმპლემენტიროთ კიდევ ერთი მეთოდი სახელად getFullInfo, რომელიც აბრუნებს სრულ ინფორმაციას შემდეგი ფორმატით

// Tesla Model S from 2015. 2 person owns this car. These are - Daniel Barbakadze, Elon Musk.
სადაც: Tesla = make; Model S = model; 2015 = year; 2 = getOwnersCount(); Daniel Barbakadze, Elon Musk = getOwnerNames(). გაითვალისწინეთ, რომ ფუნქციის მიერ დაბრუნებული სახელები გამოყოფილი უნდა იყოს მძიმით ,.

კონსტრუქტორ ფუნქცია Person-ში დავამატოთ მეთოდი getAllCarsInfo, რომელიც დააბრუნებს სრულ ინფორმაციას ყველა ავტომობილის შესახებ შესაბამის ფორმატში

// Daniel owns these cars: Tesla Model S released in 2015, BMW M2 released in 2019.
სადაც: Daniel = name; Tesla Model S released in 2015 და BMW M2 released in 2019, რომლებიც , ით არიან გამოყოფილი კი = getCarInfo();

Homework-1 Test
use this code to test your homework.

let daniel916 = new Person("Daniel", "Barbakadze", 21, "M", []);
let ilona = new Person("Elon", "Musk", 30, "M");
let duti_picoti = new Car("BMW", "525", "1999");
let stodevianosto = new Car("Mercedes", "E190", 1991);

daniel916.buysCar(duti_picoti); // adds passed car
daniel916.buysCar(stodevianosto); // adds passed car
daniel916.sellsCar(duti_picoti); // removes passed car
ilona.buysCar(stodevianosto); // adds passed car
ilona.buysCar(duti_picoti); // adds passed car

console.log({
  daniel: {
    fullName: daniel916.fullName(),
    countCars: daniel916.countCars(),
    getAllCarsInfo: daniel916.getAllCarsInfo(),
  },
  elon: {
    fullName: ilona.fullName(),
    countCars: ilona.countCars(),
    getAllCarsInfo: ilona.getAllCarsInfo(),
  },
  duti_picoti: {
    getOwnersCount: duti_picoti.getOwnersCount(),
    getOwnerNames: duti_picoti.getOwnerNames(),
    getFullInfo: duti_picoti.getFullInfo(),
    getCarInfo: duti_picoti.getCarInfo(),
  },
  stodevianosto: {
    getOwnersCount: stodevianosto.getOwnersCount(),
    getOwnerNames: stodevianosto.getOwnerNames(),
    getFullInfo: stodevianosto.getFullInfo(),
    getCarInfo: stodevianosto.getCarInfo(),
  },
});
Result must be:

{
  daniel: {
    countCars: 1,
    fullName: "Daniel Barbakadze",
    getAllCarsInfo: "Daniel owns these cars: Mercedes E190 released in 1991.",
  },
  elon: {
    countCars: 2,
    fullName: "Elon Musk",
    getAllCarsInfo: "Elon owns these cars: Mercedes E190 released in 1991, BMW 525 released in 1999.",
  },
  duti_picoti: {
    getCarInfo: "BMW 525 released in 1999",
    getFullInfo: "BMW 525 from 1999. 1 person owns this car. These are - Elon Musk.",
    getOwnerNames: ["Elon Musk"],
    getOwnersCount: 1,
  },
  stodevianosto: {
    getCarInfo: "Mercedes E190 released in 1991",
    getFullInfo: "Mercedes E190 from 1991. 2 person owns this car. These are - Daniel Barbakadze, Elon Musk.",
    getOwnerNames: (2)[("Daniel Barbakadze", "Elon Musk")],
    getOwnersCount: 2,
  },
}
