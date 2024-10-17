class Stack {
    private int[] stack = new int[10];
    private int top = -1;

    public void push(int value) {
        if (top >= 9) {
            System.out.println("Stack Overflow");
        } else {
            stack[++top] = value;
            System.out.println(value + " pushed into stack.");
        }
    }

    public void pop() {
        if (top < 0) {
            System.out.println("Stack Underflow");
        } else {
            int value = stack[top--];
            System.out.println(value + " popped from stack.");
        }
    }

    public void display() {
        if (top < 0) {
            System.out.println("Stack is empty.");
        } else {
            System.out.print("Stack elements: ");
            for (int i = 0; i <= top; i++) {
                System.out.print(stack[i] + " ");
            }
            System.out.println();
        }
    }
}

public class StackTest {
    public static void main(String[] args) {
        Stack stack = new Stack();
        stack.push(10);
        stack.push(20);
        stack.push(30);
        stack.display();
        stack.pop();
        stack.display();
    }
}
