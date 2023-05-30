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
