class Element {
  constructor(tagName) {
    this.tagName = tagName
    // reference to other elements
    this.parent = null
    this.children = []
    this.prev = null
    this.next = null
  }
render(){
      let childFragment = ``
      this.children.forEach(child => childFragment += child.render())
      
      return `<${this.tagName}>${childFragment}</${this.tagName}>`
  }
appendChild(child){
    if(child instanceof Element){
        this.children.push(child)
    } else {
      //  console.log(Object from class "${child.constructor.name}" does not belong to the class Element !)
    }
  }
removeChild(child){
    if(child instanceof Element){
        for(let i=0;i<=this.children.length-1;i++){
            let obj = Object.is(this.children[i], child); 
              if(obj){
                    this.children.splice(i,1)
                    console.log(this.children)
              }
        }
     }
 }
}

//############################## the another class
class Error{
  constructor(name) {
    this.name = name
  }
}
//################################# the another class

   let parent = new Element("div")
  let h1 = new Element("h1")
  parent.appendChild(h1)
  parent.appendChild(new Element("p"))
  parent.removeChild(h1) // remove because exists object h1 in class Element
  parent.removeChild(new Element("p")) //nu il putem sterge din clasa, fiindca in functia Object.is() nu recunoaste obiectul nou creat si nu il poate compara(exceptii la Object.is())
  
  console.log(parent.render())
