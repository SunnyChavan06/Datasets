## Titanic Dataset 🛳️

The sinking of the Titanic is one of the most infamous shipwrecks in history.

On April 15, 1912, during her maiden voyage, the widely considered “unsinkable” RMS Titanic sank after colliding with an iceberg. Unfortunately, there weren’t enough lifeboats for everyone onboard, resulting in the death of 1502 out of 2224 passengers and crew.

While there was some element of luck involved in surviving, it seems some groups of people were more likely to survive than others.

In this challenge, we ask you to build a predictive model that answers the question: “what sorts of people were more likely to survive?” using passenger data (ie name, age, gender, socio-economic class, etc).
The data has been split into two groups:

1. training set (titanic_train.csv) : 891 records
2. test set (titanic_test.csv) : 418 records

The training set should be used to build your machine learning models. For the training set, we provide the outcome (also known as the “ground truth”) for each passenger. Your model will be based on “features” like passengers’ gender and class. You can also use feature engineering to create new features.

The test set should be used to see how well your model performs on unseen data. For the test set, we do not provide the ground truth for each passenger. It is your job to predict these outcomes. For each passenger in the test set, use the model you trained to predict whether or not they survived the sinking of the Titanic.

📊 Column Description

**1. PassengerId :**
- Unique identifier for each passenger.
- Just a serial number (not useful for modeling).

**2. Survived (only in train.csv) :**  🎯
- Target variable: whether the passenger survived.
- Values: 0 = No, 1 = Yes.

**3. Pclass :**
- Passenger class (a proxy for socio-economic status).
- Values:
  - 1 = 1st (Upper class)
  - 2 = 2nd (Middle class)
  - 3 = 3rd (Lower class)

**4. Name :**
- Full name of the passenger.
- Includes title (e.g., Mr., Mrs., Miss.), which can be extracted for feature engineering.

**5. Sex :**
-Gender of the passenger: male or female.

**6. Age :**
- Age of the passenger in years.
- Contains missing values.
- Can be treated as a numerical or categorical feature (e.g., child, adult).

**7. SibSp :**
- Number of siblings and spouses the passenger had aboard the Titanic.
- SibSp = Siblings + Spouse

**8. Parch :**
- Number of parents and children the passenger had aboard.
- Parch = Parents + Children

**9. Ticket :**
- Ticket number (can be alphanumeric).
- Not unique and not always useful, but sometimes ticket prefixes carry meaning.

**10. Fare :**
- Fare the passenger paid for the ticket (in British Pounds).
- Continuous numeric feature.
- Often varies with Pclass.

**11. Cabin :**
- Cabin number(s) assigned to the passenger.
- Many missing values.
- Can extract deck letter from it (e.g., C85 → C).

**12. Embarked :**
- Port of embarkation (where the passenger boarded):
  - C = Cherbourg
  - Q = Queenstown
  - S = Southampton
- Some missing values.
