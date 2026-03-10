# LAT-computational-model
# Project deadline: submission by 15 August. So work completed by 7-15 July, for adequate time to write-up thoroughly.
# Project aim: Create a coherent model implementing Zolnek et al (2026)'s "Layer 6b theory of attention", which recapitulates the key elements and predictions of the theory, in a five-stage architecture
# Stage 1: minimal dynamical-systems model – single loop: neural populations and external inputs, connectivity structure, population rate equations, and synaptic dynamics
# S1 target behaviours x3: 
# S1.1: Triggering attention in a loop - can transient non-pyramidal L6b activation switch a previously inactive loop into the active state? Protocol - low baseline $A_i$ lifting to adequate $A_i$, and briefly applying top-down $B_i^np$ pulse to loop $i$. Desired outcomes - $L_i$ and $H_i$ transition from quiescent to active; they remain active only if $B_i^p$ also becomes engaged
# S1.2: Sustained attention - does an activated loop remain active only while corresponding L6b pyramidal drive remains active? Protocol - active loop $i$, hold $P_i$ and $A$ high, then remove P_i or reduce A. Desired outcomes - with intact B_i^p, L_i <-> H_i activity (CTC loop) stays stable. Once B_i^p falls, CTC depression causes rapid collapse.
# S1.3: State dependence - does arousal gating matter (implementing orexin/arousal system excitability)? Protocol: run same triggering inputs as in S1, but in SNN model and under different $A$ levels. Desired outcome: under low $A$, top-down input fails to recruit L6b robustly. Under moderate/high $A$ topdown input successfully recruits L6b and stabilises a loop.
# Stage 2: multiple competing loops - each loop corresponds to a 'feature' and is treated as a labeled attractor. Competition via mutual inhibition between loop-level activation variables
# S2 target behaviour x1: Switching - can the model rapidly disengage one loop and engage another (attractor competition model)? Protocol - activate loop 1, then withdraw to-down input to loop 1 simultaneously providing to-down input and B_i^np pulse to loop 2. Desired outcomes - loop 1 collapses quickly and loop 2 rises quickly, with brief overlap (brevity of overlap is critical to theory's core claim about fast attentional flexibility)
# Stage 3 - Stage 5: unlikely to get this far, given my project deadline.
# Stage 3: Move from simpler rate-based model, to a spiking-network implementation (single-compartment, leaky integrate-and-fire as simplist implementation) – enables modelling of bursts, gamma oscillations, NMDA spikes/tuft effects, fast onset/offset, E/I interaction
# S3 target behaviours x5: bursts, NMDA spikes/tuft effects, fast onset/offset, E/I interaction
# Stage 4: Model neuromodulation via orexin, arousal-state signalling and top-down PFC/frontoparietal input
# S4 target behaviurs: I think just recapitulating the effects seen in the rate-based model, but in an SNN model
# Stage 5: Adjust parameters to enable gamma-like rhythmic synchronisation to emerge when a loop becomes active (via recurrent E/I cycles) and with activity corresponding to gamma-power
