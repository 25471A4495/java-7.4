import java.util.LinkedList;

class PC {

    LinkedList<Integer> list = new LinkedList<Integer>();
    int capacity = 2;

    public void produce() throws InterruptedException {

        int value = 0;

        while (true) {

            synchronized (this) {

                while (list.size() == capacity) {
                    wait();
                }

                list.add(value);

                System.out.println("Producer produced-" + value);

                value++;

                notify();
            }

            Thread.sleep(1000);
        }
    }

    public void consume() throws InterruptedException {

        while (true) {

            synchronized (this) {

                while (list.size() == 0) {
                    wait();
                }

                int value = list.removeFirst();

                System.out.println("Consumer consumed-" + value);

                notify();
            }

            Thread.sleep(1000);
        }
    }
}

public class ProducerConsumer {

    public static void main(String[] args) {

        final PC pc = new PC();

        Thread producer = new Thread(new Runnable() {
            public void run() {
                try {
                    pc.produce();
                } catch (InterruptedException e) {
                    Thread.currentThread().interrupt();
                }
            }
        });

        Thread consumer = new Thread(new Runnable() {
            public void run() {
                try {
                    pc.consume();
                } catch (InterruptedException e) {
                    Thread.currentThread().interrupt();
                }
            }
        });

        producer.start();
        consumer.start();

        try {
            producer.join();
            consumer.join();
        } catch (InterruptedException e) {
            Thread.currentThread().interrupt();
        }
    }
}