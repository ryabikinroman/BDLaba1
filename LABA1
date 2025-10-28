import scala.util.Random
import scala.io.StdIn.readInt

object SumOfPairs extends App {

  val random = new Random()
  val listSize = 10
  val numbers: List[Int] = List.fill(listSize)(random.nextInt(20)) 

  println(s"Сгенерированный список: $numbers")

  print("Введите число для ограничения суммы пары: ")
  val limit = readInt()

  def sumPairs(list: List[Int], limit: Int): Int = {
    
    val pairs = for {
      i <- list.indices
      j <- (i + 1) until list.length
      if list(i) != list(j)
      if list(i) + list(j) < limit
    } yield list(i) + list(j)

    pairs.sum
  }

  val result = sumPairs(numbers, limit)
  println(s"Сумма всех пар неравных чисел меньше $limit: $result")
}
