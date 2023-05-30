```swift

import SwiftUI


//Model-View of struct

class field: ObservableObject {
    
    @Published var category : field = .balini
    
    
    enum field {
        case balini
        case lab
        case then
    }
    
}


//Model

struct symptoms : Hashable,Decodable,Identifiable {
    var id:Int
    var name : String
    var category : String
    var state : Bool
}


  

```
