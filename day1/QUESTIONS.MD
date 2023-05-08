-How much is the current memory capacity of a canister?
-What is the issue with the following code sample?
actor {
  let counter : Nat = 0;
  public func increment_counter() : async () {
    counter := counter + 1;
  };
}

Answer: counter variable is unmutable, but with the function we're trying to redefine it which is erroneous.


-What is the issue with the following code sample?
actor {
  var message : Text = 0;

  public query func change_message(new_message : Text) : async () {
    message := new_message;
    return;
  };
  public query func see_message() : async Text {
    return(message);
  };
}

Answer: 0 is not a text, a Text variable must be quoted.


-False or True: we can remove the keyword async for the return argument of a query function since queries are faster to answer.

Answer: False, the query function must be asyncrhonous as it can be used by multiple users.