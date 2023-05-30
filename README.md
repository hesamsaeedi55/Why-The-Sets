# Why-The-Sets
You might be curious why we need to use SET in our projects. SETs are like arrays but with two differences. First, in SET items are unique, and Second, aren't stored in any order. So why shall we implement some values as set if it kinda has fewer features than an array?


# Description of Example 

Imagine we have a struct containing attributes of animal diseases. We want to create a doctor assistant app to input the symptoms of an animal in the app to get a predicted answer related to symptoms.

# The Output Video

https://github.com/hesamsaeedi55/Why-The-Sets/assets/118046088/ce09b327-6907-4716-995b-cb0feb92855a

# WHY THE SETS?!
 
## Main Reason

Because we don't need selected symptoms to be as a sorted array, we only want to know which of them are selected and it will be a duplication of code if we decide to define them in order. For example, if the user chooses the first and the second item the temp item is [item 1, item 2] while if the user selects the same but in reverse sort it would be [item 2, item 1] which makes trouble to check the temp item and we have to write two or more cases for one group of symptoms. We only need to know which items are in a temporary variable and check them in the function. Here come the sets with the feature of having no order.

## Second Reason

Since each symptom is unique, we must prevent a repeat in the selected variable. For example, if the user taps a symptom more than once the temp item that's going to get checked in function turns into duplication of a specific symptom more than once which is wrong. The Set doesn't accept duplication of an item. So if the user taps the "item 1" more than once, the temp variable still is an array with just one instance of "item 1" which is appropriate to get checked.

## third Reason

It's fast.



# here is our struct model 

```swift
struct symptoms : Hashable,Decodable,Identifiable {
    var id:Int
    var name : String
    var category : String
    var state : Bool
}
```
# here is our instances based on struct model 

```swift
  @State var example : [symptoms] = [
        symptoms(id: 0, name: "symp1", category: "balini", state: false),
        symptoms(id: 1, name: "symp2", category: "lab", state: false),
        symptoms(id: 2, name: "symp3", category: "then", state: false),
        symptoms(id: 3, name: "symp4", category: "balini", state: false),
        symptoms(id: 4, name: "symp5", category: "balini", state: false),
        symptoms(id: 5, name: "symp6", category: "then", state: false),
        symptoms(id: 6, name: "symp7", category: "balini", state: false),
        symptoms(id: 7, name: "symp8", category: "then", state: false),
        symptoms(id: 8, name: "symp9", category: "lab", state: false),
        symptoms(id: 9, name: "symp10", category: "lab", state: false),
        symptoms(id: 10, name: "symp11", category: "lab", state: false),
        symptoms(id: 11, name: "symp12", category: "then", state: false),
        symptoms(id: 12, name: "symp13", category: "balini", state: false)

   ]
```
# here is function which receives the temporary selected items as a set value


# here is function which receives the temporary selected items as a set value

```swift
 //set function
     func classifier(check: Set<Int>) {

        let firstdisease = check
        
        print(firstdisease)
        switch firstdisease {
        case [0] :
            result = "symp1"
        case [1] :
            result = "symp2"
        case [1,0] :
            result = "symp 1 , symp 2"
        case[2,3] :
            result = "symp 3 , symp 4"
        default :
            result = "none"
        }
    }
}
```
 

