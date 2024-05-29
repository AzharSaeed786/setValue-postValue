# setValue-postValue
setValue(): Agar aap UI thread par hain, tab aap setValue() ka use kar sakte hain. Ye synchronous hai aur LiveData ke value ko change karta hai. Agar aap non-UI thread par hain aur setValue() ko use karte hain, to ye IllegalStateException throw karega.

postValue(): Agar aap non-UI thread par hain, tab aap postValue() ka use kar sakte hain. Ye asynchronous hai aur LiveData ke value ko change karne ke liye UI thread par ek event queue mein ek action post karta hai. Is tarah se, agar aap background thread par ho aur LiveData ki value ko update karna chahte ho, postValue() use karna sahi hai.
