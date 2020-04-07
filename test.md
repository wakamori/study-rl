$$
\begin{align}
v_\pi(s) &\doteq \mathbb{E}_\pi[G_t|S_t=s] \\
         &= \mathbb{E}_\pi[R_{t+1}+\gamma G_{t+1}|S_t=s] \\
         &= \sum_{a}\pi(a|s)\sum_{s'}p(s'|s,a)\mathbb{E}_\pi[R_{t+1}+\gamma G_{t+1}|S_t=s,A_t=a,S_{t+1}=s'] & \text{from (3)}\\
         &= \sum_{a}\pi(a|s)\sum_{s'}p(s'|s,a)[r+\gamma\mathbb{E}_\pi[G_{t+1}|\underbrace{S_t=s,A_t=a}_{\text{ignorable}},S_{t+1}=s']] & \text{from (6)}\\
         &= \sum_{a}\pi(a|s)\sum_{s'}p(s'|s,a)\left[r+\gamma v_\pi(s')\right]
\end{align}
$$