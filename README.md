# Cyber-security-dataset-of-EDS
 \subsection{Attack model}
%The types of attacks and implementation criteria designed by attackers with different capabilities are presented, as shown in Table \ref{tab1:Attacker capabilities}. 
 The experimental platform allows for the design of attack types that cover all aspects of digital inputs, control parameters and analog inputs. The level of attack increases gradually, starting with network access and progressively acquiring the knowledge required for the attack to realize advanced stealth attacks.
 
\begin{enumerate}  
\item Access to ICS network\\
 Attackers focus on gathering information about the topology and devices in the industrial control network.    
 \begin{itemize}
     \item Information Leakage: 
     Use scanning tools to obtain critical information such as IP addresses, device models, and operating systems of the devices on the industrial control network.
   %They use scanning tools to scan the industrial control network and obtain critical information such as IP addresses, device models, and operating systems of the devices. Additionally, they scan the PLC's operational status, using SZL packets to read the PLC model, and consider a successful attack as one where they have obtained the desired target information to prepare for subsequent attacks.  
   \item Replay Attack: 
   Resend the eavesdropped data to the receiver without knowing the exact meaning of the specific data being replayed.
 \end{itemize}
\item Understand Physical Processes\\
Attackers conduct in-depth research on control programs and relevant materials to understand the physical significance of each point in the PLC. 
 \begin{itemize}
     \item Command Injection: 
     Manipulate system behavior or gain unauthorized access by inserting malicious commands into the input.
     \item Sensor Data Tampering: 
     Maliciously manipulate the parameters of sensors to deceive the system.
 \end{itemize} 
 
\item Understand Control Logic\\
Attackers possess higher technical skills. 
 \begin{itemize}
     \item Control Parameter Tampering: 
     Collect and analyze extensive normal data to gain an in-depth understanding of the system’s operational patterns and the logical relationships between different points, so as to acheive control parameter tampering. 
     \item Multi-Point Attack: 
     Adopt more covert attack methods, design multiple control commands to execute coordinated attacks, aiming to control and disrupt the system without arousing excessive suspicion.
 \end{itemize}

\item Access to Field Devices\\
Unlike the previous categories that are limited to network penetration, physical attackers can directly access the location of the control equipment through social engineering means. 
 \begin{itemize}
     \item Physical Attack: 
     Including damaging equipment, manipulating operations, or exploiting the help of internal employees to execute attacks.% Their successful attacks involve direct physical interventions to disrupt the ICS or cause abnormal operations.
 \end{itemize}
\end{enumerate}  

% \setlength{\extrarowheight}{3pt} %增加整个表格的行高，而不会影响其他部分的排版
% \begin{table}[]
%     \centering
%     \caption{Attacker capabilities and corresponding attack types}
%     \label{tab1:Attacker capabilities}
%     \begin{tabular}{ll}
%         \hline
%         \multicolumn{1}{c}{Attacker Capability}           & \multicolumn{1}{c}{Attack Type}                 \\ \hline
%         \multirow{2}{*}{Parse ICS network}                & Information Leakage                             \\ \cline{2-2} 
%                                                           & Replay Attack                                   \\ \hline
%         \multirow{2}{*}{Understand Physical Processes}    & Command Injection                               \\ \cline{2-2} 
%                                                           & Sensor Data Tampering                           \\ \hline
%         \multirow{2}{*}{Understand Control Logic}         & \multicolumn{1}{c}{Control Parameter Tampering} \\ \cline{2-2} 
%                                                           & Multi-Point Attack                              \\ \hline
%         Access to Field Devices                           & Physical Attack                                 \\ \hline
%     \end{tabular}
% \end{table}
