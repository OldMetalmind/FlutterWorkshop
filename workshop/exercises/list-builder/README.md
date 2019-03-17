# List Builder

## Setup

- Copy the content of `main.txt` into the file this folder into `/my_app/lib/main.dart`
  
## Tasks

1. Compare how different `ListBuilder(..)` is with a previous used `ListView(..)`.
2. Edit so that it only show the "Favorite Child" row, without altering "items" array
3. Replace `items` with the following: 
```
   final items = List<ListTile>.generate(10, (index) => ListTile(title:Text("Row number $index")));
```
4. What happened?
5. Experiment with the function `.filled()`
6. Edit that in a way the odd rows say "Odd row" and the even "Even row"  (tip: Int.isOdd)
7. Wrap your ListTile's with `GestureDetector(..)` so that the property onTap(..) will `print()` the row number.
   * You will need to open the Debug Console of Visual Studio Code to see the output on tap. 
8. The function print is boring.. lets call a SnackBar to show the message.
   * Use the following function to help you.

```
Widget tappableTile(context, index) {
  return GestureDetector(
      child: ... ,
      onTap: () {
        Scaffold.of(context).showSnackBar(new SnackBar(
          content: ... ,
        ));
      });
}
```
9. Make the Snackbar only show for 100 milliseconds.