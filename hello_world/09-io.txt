Standard input (stdin) e standard output (stdin)
-----------------------------------------------


Ogni comando UNIX suppone di avere un "input" ed un "output".

Spesso l'output e' il video, l'input e' la tastiera. Ma non 
e' sempre cosi'.

In un comando come grep, ad esempio, l'output e' il video.
E se volessimo l'output in un file?


Redirezione l'output
--------------------

Come anche nel DOS, l'output si puo' redirezionare verso
un file, usando il simbolo ">".


In questo esempio:

	# grep "italy" veicoli > veicoli_italiani

verra' creato il file "veicoli_italiani", contente solo 
i veicoli fatti in Italia.


Redirezione l'input
---------------------

Questo viene fatto in genere usando le "pipes".
Vedi in seguito.


Memorizzare il risulto in una variabile
----------------------------------------

Questa e' una delle caratteristiche piu' importanti di UNIX.
Grazie ad essa, l'output di un comando puo' essere memorizzato
in una variabile, invece che in un file.

Se ho usato la variabile X, per stamparne il valore devo fare "echo $X".
(notare il segno di $).

	# x=5
	# echo $x	(qui ci stampera' 5)

La sintassi per farlo e' la seguente:

		# variabile=$( comando UNIX )

Esempi:

		# lista = $(ls /bin)
		# oggi = $(date)
		# risultato=$(expr 2 + 3)



