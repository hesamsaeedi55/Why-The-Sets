```swift

//defining set variable
    @State var tempList : Set<Int> = []

    //buttons of tab
HStack {
                Text("balini")
                    .onTapGesture {
                        selectField.category = .balini
                    }
                Text("lab")
                    .onTapGesture {
                        selectField.category = .lab
                    }
                
                Text("then")
                    .onTapGesture {
                        selectField.category = .then
                    }

            }


 //set function
   func classifier(check: Set<Int>) {
        
        
//        var tr = check["a"]?.description
//        tempResult = tr!
        
        let firstdisease = check
        
        print(firstdisease)
        switch firstdisease {
        case [0] :
            result = "0"
        case [1] :
            result = "1"
        case [1,0] :
            result = "01"
        case[2,3] :
            result = "23"
        default :
            result = "none"
        }
    }
}

```
