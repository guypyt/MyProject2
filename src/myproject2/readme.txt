1. (5 points) create a public "Grade062" enum in the "util.pootorn" package. 
   "Grade062" has the following values: GOOD, AVERAGE, POOR, and NONE respectively.

2. (45 points) Given the public "Comment" class in the "util.pootorn" package, 

/** --------------------------------------------
public class Comment {
   private final String message;
   public Comment062(String message) { this.message = message; }
   @Override
   public boolean equals(Object obj) {
      if (this == obj) return true;
      if (obj == null || getClass() != obj.getClass()) return false;
      return message.equals(((Comment) obj).message);
   }
   @Override public int hashCode() { return message.hashCode(); }
   protected String getContent() { return message; }
   @Override public String toString() { 
      return this.getClass().getSimpleName() + "(" + getContent() + ")"; 
   }
}
-------------------------------------------- **/

2.1 (3 points) create a public "CommentPlus062" class (in the "util.NNNNN" package) 
    that extends the "Comment" class.  You must not modify anything in 
    the "Comment" class.  The "CommentPlus062" class must contain 
    the following members (i.e., fields & methods).

2.2 (2 points) "grade062" which is a private final field of "Grade062" type.

2.3 (10 points) "GRADE062_COMPARATOR" which is a public static final field 
    of "Comparator<CommentPlus062>" type. The value of this field is 
    a lambda expression for comparing 2 "CommentPlus062" 
    by comparing their "grade062".

2.4 (10 points) a public static "match062(...)" method that receives 
    a "grade" parameter of "Grade062" type and returns "Predicate<CommentPlus062>" 
    type. This method returns a lambda expression.  This lambda expression receives 
    a "CommentPlus062" object and returns true if the grade062 of that object 
    equals the "grade" parameter. Otherwise, this lambda expression returns false.

2.5 (10 points) a public constructor that receives a "message" of "String" type
    and a "grade" of "Grade062" type. This constructor must call the constructor 
    of its supertype ("Comment") with the "message" as the parameter.
    If "message" is null, it initializes the "message" field to "NO_COMMENT" instead.
    If "grade" is null, it initializes the "grade062" field to Grade062.NONE instead.

2.6 (10 points) a protected "getContent()" method that overrides its superclass's method.
    This method returns a String which consisting of (1) the result string from 
    its superclass's getContent() method, concatenating with (2) the result string 
    from its grade062 field.  Note that if its grade062 field is null, 
    it concatenates an empty String instead of null.

3. (12 points) Given the public "Commentable" interface in the "commenting.NNNNN" package,

/** --------------------------------------------
public interface Commentable extends Iterable<CommentPlus062> {
   default boolean addComment(String message) { return addComment(message, null); }
   boolean addComment(String message, Grade grade);
   boolean removeComment(String message);
   Iterator<CommentPlus062> iterator();
   Collection<String> extract(Grade062 grade);
   void sort();
}
-------------------------------------------- **/

3.1 (2 points) create a public "CommentablePlus062" interface 
    (in the "commenting.062" package) that extends "Commentable" interface. 
    The "CommentablePlus062" interface must contain the following methods.

3.2 (10 points) a default "inspect062()" method that returns a String. 
    This method uses the iterator of its super-interface to iterate 
    over all comments, convert them to Strings, and returns 
    the concatenation of those Strings.

4. (45 points) From the "CommentablePlus062" interface in the previous question,

4.1 (2 points) create a public "CommentList062" class 
    (in the "commenting.pootorn" package) that implements 
    "CommentablePlus062" interface.  The "CommentList062" class 
    must contain the following field and overriding methods.

4.2 (3 points) a "comments062" field that is a private final field 
    of "LinkedList<CommentPlus062>" type, and initializes to 
    a newly-created LinkedList.

4.3 (10 points) a "addComment(...)" method that returns true if it adds 
    the comment message with the grade to the "comments" field successfully.
    Otherwise, it returns false. It will not add the comment message with 
    the grade if the comment message is null.

4.4 (10 points) a "removeComment(...)" method that returns true if it removes 
    the first comment containing the given message (in the parameter) from 
    the "comments062" field successfully.  Otherwise, it returns false. 
    It will not remove the comment if the comment message is null.
 
4.5 (5 points) an "iterator()" method that returns the iterator of 
    the "comments062" field.

4.6 (5 points) a "sort()" method that sorts the "comments062" field 
    using the "GRADE062_COMPARATOR" of the "CommentPlus062" class.

4.7 (10 points) an "extract(...)" method that returns a String Collection of 
    all comment messages in the "comments062" field that matches ("match062")
    the grade parameter.

END --------------------------------------------------------------
