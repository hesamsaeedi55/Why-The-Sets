# Why-The-Sets
You might be curious why we need to use SET in our projects. SETs are like arrays but with two differences. First, in SET items are unique, and Second, aren't stored in any order. So why shall we implement some values as set if it kinda has fewer features than an array?


# Description of Example 

Imagine we have a struct containing attributes of animal diseases. We want to create a doctor assistant app to input the symptoms of an animal in the app to get a predicted answer related to symptoms.

# The Output Video



https://github.com/hesamsaeedi55/Why-The-Sets/assets/118046088/ce09b327-6907-4716-995b-cb0feb92855a

# WHY THE SETS?!
 
## Main Reason

Because we don't need selected symptoms to be as a sorted array, we just want to know which of them are seelcted and it will be a duplication of code if we decide to define them in order. For example, if user chooses the first and the second item the temp item is [item 1, item 2] while if the user select the same but in reverse sort it would be [item 2, item 1] which makes a trouble to check the temp item and we have to write two or more cases for one group of symptoms. We just need to know which items are in temporary variable and just check them in the function. Here comes the sets with feature of having no order.

## Second Reason



# here is our struct model 

```swift
struct symptoms : Hashable,Decodable,Identifiable {
    var id:Int
    var name : String
    var category : String
    var state : Bool
}
```

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
 

